# Using labels

This guideline describes the best practices related to using Github Labels for Issues and Pull Requests.

## Note

The procedure described in this guideline does only apply to Polypheny-DB and not to the other projects.

## Label categories

Contributors with sufficient permissions on the Polypheny-DB repo can help by adding
labels to issues and (to a lesser degree) pull requests:

* Yellow, **A**-prefixed labels state which **area** of the project an issue
  relates to. Examples: A-core, A-ui, A-stores

* Light purple, **C**-prefixed labels represent the **category** of an issue.

* Green, **E**-prefixed labels explain the level of **experience** necessary
  to fix the issue.

* The light orange **invalid** label marks an issue as being opened in error.

* The purple **metabug** label marks lists of bugs collected by other
  categories.

* Orange, **P**-prefixed labels indicate a bug's or issue's **priority**.

* Gray, **S**-prefixed labels are used for tracking the **status** of pull
  requests.

## Labeling pull requests

There are mainly two labels that should be used for pull requests:

* **S-waiting-on-review**, the pull request is ready to be reviewed. If your PR is not ready, 
  consider using a draft pull request.

* **S-waiting-on-author**, the pull request requires changes by the author.

Other possible labels:

* **S-blocked**, something is blocking this pull request from being merged. If you assign this label,
  please also leave a comment that states what is blocking, esp if there is an issue that can be referenced.

* **S-inactive**, there has been no activity for some time.

* **P-critical**: This pull request must be reviewed and merged as soon as possible.

## Credits

This labeling scheme is based directly on the [Rust language repository](https://github.com/rust-lang/rust/). 
The rust project is dual-licensed under Apache 2.0 and MIT terms.

