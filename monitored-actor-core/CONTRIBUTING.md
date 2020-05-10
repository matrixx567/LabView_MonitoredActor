# Contributing

## Guidelines

These guidelines will ensure the pull request process is easy and traceable for the contributor and maintainer.

* When contributing to this repository, please first discuss the change you wish to make via issue,
  email, or any other method with the owners of this repository before making a change.
* Keep changes concise and encapsulated. If you have multiple features/fixes to implement, make sure to keep each implementation isolated in to one pull request. Large pull requests will be declined.
* If you're unsure of how to fix a bug or implement a feature create an issue instead. The maintainers will monitor new issues and decide how tp proceed.
* All new features and bug fixes require a unit tests that adequately test the feature.

## Pull Request Process

### Setting up your environment

1.  Install the appropriate version of LabVIEW. See the [README](readme.md) for information about LabVIEW version compatibility.
2.  Fork this repository.
3.  Install GPM dependencies using the `gpm install` command.

### Publishing your change

1.  Increase the version number in gpackage.json and create new entry at the beginning of [CHANGELOG](changelog.md). Entries in the changelog file should be quick bullet points of the items changed, not just commit messages. The versioning scheme we use is [SemVer](http://semver.org/).
2.  Submit the pull request. A maintainer will review the changes contact you with any followup actions.

#### Contact [support@mooregoodideas.com](mailto:support@mooregoodideas.com) with any questions
