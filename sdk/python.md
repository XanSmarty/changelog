# [Python SDK](https://smartystreets.com/docs/sdk/python)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [4.4.1] - 2020-02-26

### Changed:

- Fixed bug that made the autocomplete client crash if there are no suggestions in the response.

## [4.4.0] - 2019-11-25

### Changed:

- Return input id with result.
- Comment added to clarify match strategy.


## [4.3.0] - 2019-06-05

### Changed:

- Populated relevant input fields in examples.
- New custom header option available in client builder.


## [4.2.0] - 2019-03-13

### Changed:

- Moved changelog.
- Changes structure added to analysis in international street API. Rootlevel created to accomodate.


## [4.1.0] - 2019-02-25

### Changed:

- Introduced the `ews_field` to the `metadata` section of the US Street API response.
- Deprecated the `ews_field` on `analysis` section of US Street API response. (The `ews_match` field has never been part of the analysis section.)


## [4.0.1] - 2019-01-14

### Changed:

- Re-introduced dependency on twine for uploading new releases to PyPI.

## [4.0.0] - 2019-01-14

### Changed:

- Moved `__version__` variable to its own module to remove installation dependency on `requests` module.

## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-python-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-python-sdk/compare/4.0.1...HEAD
[4.0.1]: https://github.com/smartystreets/smartystreets-python-sdk/compare/4.0.0...4.0.1
[4.0.0]: https://github.com/smartystreets/smartystreets-python-sdk/compare/3.3.2...4.0.0
[Earlier]: https://github.com/smartystreets/smartystreets-python-sdk/releases
