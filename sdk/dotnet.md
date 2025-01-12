# [.Net SDK](https://www.smarty.com/docs/sdk/dotnet)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [8.14.0] - 2023-07-06

### Changed:

- Added smarty_key field to us-street api.


## [8.13.19] - 2023-06-27

### Changed:

- Added "source" input and output fields to US Reverse Geo.


## [8.13.18] - 2023-02-17

### Changed:

- Added matching strategy support in the US Extract api client


## [8.13.17] - 2023-01-25

### Changed:

- Added new constants in international-autocomplete-api for use with the geolocation parameter:
    - "adminarea", "locality"


## [8.13.16] - 2023-01-24

### Changed:

- Added new input fields in international-autocomplete-api:
    - distance, geolocation, latitude, longitude
- Added new fields in international-autocomplete-api results:
    - super_administrative_area, sub_administrative_area


## [8.13.12] - 2022-11-08

### Changed:

- Added new fields in international-street:
    - administrative_area_short, administrative_area_long, level_type, level_number


## [8.13.8] - 2022-05-10

### Changed:

- US Street examples default to us-core-cloud license.


## [8.13.7] - 2022-04-07

### Changed:

- Content type being set directly on the request rather than the header.


## [8.13.6] - 2022-04-06

### Changed:

- Sleep for 5 seconds on 429 status code.


## [8.13.5] - 2022-03-04

### Changed:

- Add Content-Type when sending a batch.


## [8.13.4] - 2022-03-02

### Changed:

- Messages in US Street examples are more accurate pertaining to address validity.


## [8.13.3] - 2022-01-04

### Changed:

- Default candidates is 5 for enhanced matching.


## [8.13.2] - 2021-12-14

### Changed:

- Code to access static credentials in US Autocomplete Pro provided in example.


## [8.13.1] - 2021-11-22

### Changed:

- Docker build uses mcr rather than dockerhub
- Fixes to how filters are delimited in US Autocomplete Pro


## [8.13.0] - 2021-10-15

### Changed:

- Support for International Autocomplete API.


## [8.12.0] - 2021-09-23

### Changed:

- Source field added to US Autocomplete Pro lookup.


## [8.11.3] - 2021-08-20

### Changed:

- Removed Autocomplete Basic example.


## [8.11.2] - 2021-08-13

### Changed:

- Autocomplete Pro example leverages proper "none" geolocation type.


## [8.11.1] - 2021-08-09

### Changed:

- Corrected geolocation type "none".


## [8.11.0] - 2021-07-14

### Changed:

- New match strategy "enhanced".


## [8.10.2] - 2021-07-13

### Changed:

- Syntax errors resolved in examples.


## [8.10.1] - 2021-07-06

### Changed:

- Removed match_mode, renamed match_details to enhanced_match.


## [8.10.0] - 2021-06-11

### Changed:

- License field descriptions in the examples.
- US Street enhanced matching integration fields in Analysis.


## [8.9.0] - 2021-03-23

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`
- Functionality added to handle the US Autocomplete Pro API.


## [8.8.0] - 2021-03-12

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`

## [8.7.1] - 2020-10-19

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.

## [8.7.0] - 2020-10-17

### Changed:

- Functionality added to handle the new US Reverse Geocoding API.

## [8.6.1] - 2020-09-30

### Changed:

- Fixed issue of InputID not being returned on batch lookups.

## [8.6.0] - 2020-08-21

### Changed:

- User can now specify the license to be used.

## [8.5.0] - 2020-03-17

### Changed:

- Incorporates Client-specific marker interfaces.

## [8.4.1] - 2020-02-06

### Changed:

- Documentation in streetapi-single to assist in creating custom url endpoint.

## [8.4.0] - 2019-12-03

### Changed:

- Added custom header sender.

## [8.3.1] - 2019-11-25

### Changed:

- Fixed syntax error in international street example.
- Comment added to clarify match strategy.


## [8.3.0] - 2019-09-25

### Changed:

- Populated relevant input fields in examples.
- Added notes for readability.
- US Street example (.vb) updated to work with library.
- Made USStreetSingleAddressExample.vb compile.
- 'inputID' added to the response.


## [8.2.0] - 2019-03-13

### Changed:

- Added Match Strategy to examples.
- Moved changelog.
- 'changes' field added to International Street Analysis, Rootlevel created to assist.


## [8.1.1] - 2019-02-26

### Changed:

- Made Analysis compile.


## [8.1.0] - 2019-02-26

### Changed:

- Update integration test to check environment variables to enable alternative API URLs (`SMARTY_URL_INTERNATIONAL_STREET`, `SMARTY_URL_US_AUTOCOMPLETE`, `SMARTY_URL_US_EXTRACT`, `SMARTY_URL_US_STREET`, `SMARTY_URL_US_ZIP`).
- Deprecated Analysis.IsEWS_Match


## [8.0.15] - 2019-01-15

### Changed:

- By default add `Accept-Encoding: gzip` header to request and handle gzipped response.


## [8.0.14] - 2018-09-18

### Changed:

- Settled on approach to leveraging docker to develop and publish.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-dotnet-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.14...HEAD
[8.0.15]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.14...8.0.15
[8.0.14]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.13...8.0.14
[Earlier]: https://github.com/smartystreets/smartystreets-dotnet-sdk/releases
