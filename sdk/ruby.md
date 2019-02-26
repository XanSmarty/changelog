# [Ruby SDK](https://smartystreets.com/docs/sdk/ruby)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [Unreleased]

### Changed:

- Nothing yet.


## [5.6.0] - 2019-02-25

### Changed:

- Introduced the `ews_field` to the `metadata` section of the US Street API response.
- Deprecated the `ews_field` on `analysis` section of US Street API response. (The `ews_match` field has never been part of the analysis section.)
- Using `warn` instead of `log` to avoid conflict with builtin function.

## [5.5.4] - 2018-09-18

### Changed:

- Standardized `Makefile`.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-ruby-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-ruby-sdk/compare/5.5.4...HEAD
[5.5.4]: https://github.com/smartystreets/smartystreets-ruby-sdk/compare/5.5.3...5.5.4
[Earlier]: https://github.com/smartystreets/smartystreets-ruby-sdk/releases
