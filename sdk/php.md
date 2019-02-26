# [PHP SDK](https://smartystreets.com/docs/sdk/php)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [Unreleased]

### Changed:

- Nothing yet


## [4.6.2] - 2019-02-25

- Extra build.


## [4.6.1] - 2019-02-25

- Extra build.


## [4.6.0] - 2019-02-25

- Introduced the `ews_field` to the `metadata` section of the US Street API response.
- Deprecated the `ews_field` on `analysis` section of US Street API response. (The `ews_match` field has never been part of the analysis section.)
- Update integration test to check environment variables to enable alternative API URLs (`SMARTY_URL_INTERNATIONAL_STREET`, `SMARTY_URL_US_AUTOCOMPLETE`, `SMARTY_URL_US_EXTRACT`, `SMARTY_URL_US_STREET`, `SMARTY_URL_US_ZIP`).


## [4.5.7] - 2019-01-15

### Changed:

- By default add `Accept-Encoding: gzip` header to request and handle gzipped response.


## [4.5.6] - 2018-09-18

### Changed:

- Standardized `Makefile`.
- Push latest commits to repo when running `make publish`.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-php-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-php-sdk/compare/4.5.6...HEAD
[4.5.6]: https://github.com/smartystreets/smartystreets-php-sdk/compare/4.5.5...4.5.6
[Earlier]: https://github.com/smartystreets/smartystreets-php-sdk/releases
