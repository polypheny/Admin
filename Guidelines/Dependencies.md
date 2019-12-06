# Dependency Guidelines

This guideline describes the best practices for including java dependencies via gradle in Polypheny.

## Version numbers

To ensure that all subprojects use the same version of a dependency, the version numbers are stored in `gradle.properties`.

The `build.gradle` file should look like this:
```groovy
dependencies {
    compile group: "com.example". name: "example-lib", version: example_lib_version
}
```

You then also have to add an entry for it in `gradle.properties`:
```
...
example_lib_version = 23.1.2
...
```

## Related issues/pull requests:
- [Different declared dependency versions between subprojects](https://github.com/polypheny/Polypheny-DB/issues/89)
- [Dependency version consolidation](https://github.com/polypheny/Polypheny-DB/pull/91)

