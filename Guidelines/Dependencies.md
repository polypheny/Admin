# Dependency Management

This guideline describes the best practices for including java dependencies via gradle in Polypheny-DB. 

## 'java-library'

Polypheny-DB is now using the `java-library` plugin instead of the `java` plugin for most of its subprojects.
`java-library` expands the capabilities of `java`, so everything that was possible before is still possible.
You can read more about `java-library` [in the official documentation](https://docs.gradle.org/current/userguide/java_library_plugin.html).

### Adding dependencies

The major difference is the introduction of two new configurations, `api` and `implementation`, which should 
be used instead of `compile` to include dependencies.

#### API
If you want to include a dependency and make it available to all other subprojects that have your project as a dependency, 
please use the `api` configuration.
```groovy
dependencies {
    api group: "com.example", name: "example-lib", version: example_lib_version
}
```

#### Implementation
If a dependency is simply required to implement your functionality but should not be available to subprojects that include 
your project, then use `implementation`.
```groovy
dependencies {
    implementation group: "com.example", name: "example-lib", version: example_lib_version
}
```

### Special case: 'dbms'

The `dbms` subproject is not using the `java-library` plugin, as it is not a library but the final product.


## Version numbers

To ensure that all subprojects use the same version of a dependency, the version numbers are stored in `gradle.properties`.

The `build.gradle` file should look like this, note the `version` part:
```groovy
dependencies {
    implementation group: "com.example", name: "example-lib", version: example_lib_version
}
```

You then also have to add an entry for it in `gradle.properties`:
```
...
example_lib_version = 23.1.2
...
```

## Note
The procedure described in this guideline does only apply to Polypheny-DB and not to the other projects.

## Related issues/pull requests:
- [Different declared dependency versions between subprojects](https://github.com/polypheny/Polypheny-DB/issues/89)
- [Dependency version consolidation](https://github.com/polypheny/Polypheny-DB/pull/91)

