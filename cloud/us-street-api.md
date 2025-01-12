# Changelog - [US Street Address API](https://www.smarty.com/docs/cloud/us-street-api)

All notable changes to the US Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 5.7.6 - 2023-08-10
Enhanced Match Improvements:
  - Fixed multiple false positive issues.
  - Fixed issue where input in street2 field occasionally returned odd results.
  - Fixed issue where M.L.K was not being recognized as a valid street.
  - Fixed issue where a duplicate PMB value was being copied into the primary number as well as PMB number field.
  - Fixed issue where some odd secondaries were being corrected erroneously.
  - Improved handling of some addresses with odd secondaries.
  - Improved capability to differentiate between street suffixes and street names.

## 5.7.2 - 2023-08-02
  - Includes a fix for when "via" or "plaza" was not being recognized.
  - Internal code optimizations.

## 5.7.1 - 2023-07-19
CHANGES:
  - Implemented USPS Cycle "O", the most notable change affects dpv_footnotes.
  - Of particular note, the meaning of the "CC" and "N1" dpv_footnotes are being revised.
  - For more information see https://www.smarty.com/docs/usps-cycle-o and https://www.smarty.com/docs/cloud/us-street-api#analysis

KNOWN ISSUES:
  - USPS has confirmed an issue in the July Cycle "O" release where some street names beginning with words such as "via" or "plaza" may not be found unless you leave those words out.
  - A fix will be available in the August data release.

## 5.6.1 - 2023-06-30
- Internal code optimizations.

## 5.6.0 - 2023-06-29
- Made smarty_key available for enhanced matching (cloud version).  

## 5.5.10 - 2023-06-23
- Fixed a minor JSONP issue where an extra header was being checked for JSONP.

## 5.5.9 - 2023-06-22
- Fixed some cases where PMB was not being returned correctly.
- Fixed issue where enhanced_match would sometimes display "none" instead of "postal-match".
- Fixed issue where Unique Zip Codes were not behaving as expected and in some cases an incorrect match was being made.

## 5.5.7 - 2023-05-05

- Fixed JSONP


## 5.5.6 - 2023-05-04

- Fixed HTTP 404 issues that would occur when a trailing slash was used at the end of the route in the URL such as https://us-street.api.smartystreets.com/street-address/?...
- Fixed HTTP 406 issues that would occur if all values in the Accept header were not supported. It will now default to return JSON in that case.
- Fixed an issue when making an API call in a web browser where it would return XML instead of JSON. 


## 5.5.1 - 2023-05-01

On-Premise customers should see documentation updates (https://www.smarty.com/docs/local/us-street-api#manage) as there are changes in the way the program is launched.

- Restructured source code to improve performance.
- Enhanced error messages which are returned as JSON with additional information.
- Geocodes are now rounded to the 6th decimal place instead of being truncated to the 6th.
- Fixed an issue where no results would be found if street2 was populated but street was not.


## 5.4.1 - 2023-04-14 - 2023-04-17

NOTE: This version will be released over the dates above.

On-Premise builds will require updated data which will be available after the cloud roll out is completed.

CHANGES:
- Enhanced accuracy and availability of geocodes.
- Improved secondary matches in enhanced mode.
- Internal code changes to prepare for upcoming features.

BUG FIXES:
- Fixed enhanced_match flag issue with strict and invalid mode when submitting batches.

## 5.3.6 - 2023-03-21

- Small internal changes regarding plans and subscriptions to interpret appropriate features of a customer request.
- Compiled using Go v1.19.7.

## 5.3.4 - 2022-01-26

CHANGES:
- Added CPR to CMR to support new data changes.
- Improved search capabilities for some alternate cities.

BUG FIXES:
- Resolved issue with outputs when secondaries were submitted in the 'street2' field.
- Resolved issues with specific key-words being dropped.

## 5.3.3 - 2022-12-08

CHANGES:

- Internal restructuring, no external changes.


## 5.3.2 - 2022-12-03

BUG FIXES:

- Fixed minor issue where a specific string combination would cause the request to fail.

## 5.3.1 - 2022-12-01

CHANGES:

Enhanced Mode Improvements:
- Significant improvements to footnotes analysis.
- Minor enhancement for misspelled street names.
- Minor improvement to match rates for addresses with similar street names.

## 5.3.0 - 2022-10-26

CHANGES:

Enhanced Mode Improvements:
- Improved match rates.
- Field enhanced_match is now consistently populated in the returned results.
- Field enhanced_match contains "ignored-input" parameter when input is not used to obtain a match.
- HC and HCR address matching has been improved.
- dpv_footnotes and footnotes are more consistent.
- Significant improvements to invalid secondaries.
- Improved matches for valid secondaries.


## 5.2.1 - 2022-09-28

## 5.2.2 - 2022-10-04

CHANGES:

- Compiled against Go v1.19.1
- Improved invalid secondary detection with hyphens in enhanced mode


## 5.2.1 - 2022-09-28

CHANGES:

- Fixed issue with invalid secondaries combining incorrectly across addresses in enhanced mode.
- Improved invalid secondary detection in enhanced mode.


## 5.2.0 - 2022-08-31

CHANGES:

- Improved speed and accuracy in enhanced mode.
- Improved primary number handling in enhanced mode.


## 5.1.1 - 2022-07-19

CHANGES:

- Compiled against Go v1.18.4.
- Upgrade to latest dependencies.
- Enhance geocode precision in very rare correction cases (cloud version).
- Internal update to DNS handling (cloud version).


## 5.0.31 - 2022-06-09

CHANGES:

- Compiled against Go v1.18.3.
- Increased load speed for local version.
- Improved street2 field recognition in enhanced mode.
- Improved secondary handling in enhanced mode.
- Improved match rates in enhanced mode.
- Improved spelling corrections in enhanced mode.


## 5.0.28 - 2022-05-04

CHANGES:
- Internal restructuring.
- Invalid secondary handling improvements for enhanced mode.

## 5.0.27 - 2022-03-23

CHANGES:

- Compiled against Go v1.17.8.
- Upgrade to latest dependencies.
- Internal restructuring, no external changes.

## 5.0.25 - 2022-02-22

CHANGES:

Enhanced Mode:
- Improved accuracy of analysis flags.
- Improved accuracy for addresses containing hyphens.
- Improved accuracy for ambiguous addresses.
- Improved accuracy for addresses containing Highways and "Heights".
- Improved accuracy when invalid zip codes are detected as input.
- Improved invalid secondary handling.

## 5.0.22 - 2021-12-6

CHANGES:

- Increased match accuracy for invalid zip codes in enhanced mode.
- Increased match accuracy for batched addresses in enhanced mode.

BUG FIXES:

- Fixed issue with invalid secondaries producing incorrect results.

## 5.0.21 - 2021-10-27

CHANGES:

- DPVMatchCode is no longer cleared in enhanced mode.
- Increased match accuracy for enhanced mode.
- Updated "enhanced" data format for local version; a new download of the "enhanced" data is required.

BUG FIXES:

- Fixed an instance where a secondary component field could be duplicated in the result under enhanced mode with non-postal data.

## 5.0.20 - 2021-08-31

CHANGES:

- Updated component input results to be more consistent with freeform input results in enhanced mode.
- Expanded multiple candidate support in enhanced mode.

BUG FIXES:

- Fixed instances where a secondary component field could be duplicated in the result under enhanced mode.

## 5.0.16 - 2021-08-12

BUG FIXES:

- Resolved issue where some queries would not return consistent results.

## 5.0.14 - 2021-08-11

BUG FIXES:

- Fix empty response for specific mangled address pattern.

## 5.0.12 - 2021-08-03

CHANGES:

- Changes to enhanced mode to eliminate some false positive results.
- Several internal changes that do not affect the user experience.  
- Provided enhanced mode for local installations (does not affect cloud environment). 

## 5.0.7 - 2021-07-14

BUG FIXES:

- In enhanced mode, a DPV match code might not have been returned in some circumstances when the match was a valid USPS address.

## 5.0.6 - 2021-07-13

In this major version release, new features are exposed via new `match` options (see [documentation](https://www.smarty.com/docs/cloud/us-street-api#input-fields)). The input/output contracts for existing features are preserved.

CHANGES:

- Release enhanced match mode and non-postal address features for cloud environments.

## 4.8.7 - 2021-05-14

BUG FIXES:

- Fixed segfault for certain startup error messages on local install.

## 4.8.6 - 2021-04-26

CHANGES:

- Updated internal metric instrumentation.

## 4.8.3 - 2021-03-05

BUG FIXES:

- Fixed issue with RDI data not being returned correctly in some cases.

## 4.8.2 - 2021-03-03

BUG FIXES:

- Fixed logging issue during spelling correction.

## 4.8.0 - 2021-02-17

CHANGES:

- Added output field: dpv_no_stat. This is a specialized field that should only be used by those who understand what it means.

## 4.7.3 - 2021-02-02

BUG FIXES:

- Fixed an issue with the on-premise binary. This did not affect cloud functionality.

## 4.7.2 - 2021-01-27

CHANGES:

- Corrected local install to not try to load unexpected data files.
- Internal restructure to better support reporting process speed to supports SLAs in hosted, cloud environment.

## 4.6.0 - 2020-11-23

CHANGES:

- Upgraded address processing engine to latest version.

- The `active` field in the `analysis` structure of the result candidate will
now always return "Y" to indicate active. In previous releases we were too
aggressive about showing a potential address as not active which could,
depending upon client processing logic, result in a perfectly valid and active
address from being utilized.


## 4.5.4 - 2020-10-29

CHANGES:

- Internal restructuring, no external changes.


## 4.5.3 - 2020-10-26

CHANGES:

- Latest dependencies.
- More attempts to geocode an address.


## 4.5.2 - 2020-10-16

CHANGES:

- Using earlier version of shared library which doesn't segfault on malformed input.
- Improved initialization speed with concurrency.


## 4.5.1 - 2020-10-15

CHANGES:

- Increased diagnostic message verbosity on failure.
- New diagnostic message regarding required number file descriptors.


## 4.5.0 - 2020-10-14

CHANGES:

- Internal structural changes.
- Removed dynamic geocoding corrections in favor of daily rotation.
- Wireup more tolerant of optional files.

## 4.4.1 - 2020-09-30

CHANGES:

- Compiled using Go v1.15.x.
- Internal structural changes.


## 4.4.0 - 2020-09-09

CHANGES:

- New `coordinate_license` field in response to give attribution as well as indicate any restrictions that may exist relative to the geocode coordinate being returned.


## 4.3.13 - 2020-08-21

CHANGES:

- Internal structural changes


## 4.3.5 - 2020-08-11

CHANGES:

- Set upper limit on number of workers for machines with high numbers of CPU cores.


## 4.3.2 - 2020-08-03

CHANGES:

- Better internal error checking surrounding geocoding.


## 4.3.1 - 2020-08-03

CHANGES:

- Internal handling of feature flags.


## 4.3.0 - 2020-07-31

CHANGES:

- Upgrade to latest dependencies
- Small internal improvements in preparation for soon-to-be-released features.


## 4.2.4 - 2020-06-12

CHANGES:

- Upgrade to latest dependencies
- Updated packaging instructions for on-premise builds.


## 4.2.3 - 2020-06-10

CHANGES:

- Compiled against Go v1.14.4.
- Adjusted internal metrics reporting frequency.

## 4.2.2 - 2020-05-28

CHANGES:

- Compiled against Go v1.14.3.
- Includes the new usps/ams libraries.

## 4.2.1 - 2020-05-05

CHANGES:

- Internal behavior surrounding subscription management.


## 4.2.0 - 2020-04-13

CHANGES:

- Updated packaging instructions for on-premise builds.


## 4.1.1 - 2020-03-24

CHANGES:

- Internal packaging and dependency management.


## 4.1.0 - 2020-03-24

CHANGES:

- Internal packaging and dependency management.


## 4.0.30 - 2020-03-17

BUG FIXES:

- Corrected concurrent access bug that caused intermittent geocode inaccuracies.


## 4.0.29 - 2020-03-16

CHANGES:

- Latest internal dependencies.


## 4.0.28 - 2020-03-13

CHANGES:

- Replace common misspellings in street input field

## 4.0.27 - 2019-12-20

CHANGES:

- Internal refactoring 


## 4.0.26 - 2019-12-19

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.


## 4.0.21 - 2019-10-22

CHANGES:

- Latest version of internal dependencies.


## 4.0.20 - 2019-10-17

CHANGES:

- Refined certain log messages and updated to latest internal dependencies.


## 4.0.19 - 2019-09-18

CHANGES:

- Better handling of freeform inputs with stray punctuation.


## 4.0.18 - 2019-09-06

CHANGES:

- Internal refactoring.


## 4.0.17 - 2019-09-06

CHANGES:

- Latest version of internal, upstream dependencies.


## 4.0.16 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.


## 4.0.15 - 2019-08-02

CHANGES:

- Latest internal dependencies.


## 4.0.14 - 2019-07-26

CHANGES:

- Slight change to internal boilerplate code used in development and testing.


## 4.0.12 - 2019-07-26

CHANGES:

- Latest internal dependencies.


## 4.0.11 - 2019-07-26 [YANKED: cloud installation]

BUG FIXES:

- Reinstated top-level /lib folder into the local installation package (required reworking much of the source code boilerplate).

CHANGES:

- Internal refactoring.
 

## 4.0.10 - 2019-07-12 [YANKED: local installation]

BUG FIXES:

- Corrected mishandling of lookups that contain no street information, introduced in the 4.0.0 release.


## 4.0.7 - 2019-07-09 [YANKED: local installation]

BUG FIXES:

- With the 4.0.0 release a concurrency-related bug was introduced in a hash calculation which caused the application to panic and shut down. (See incident details: https://status.smarty.com/incidents/dk5ghfl03vjf) This release fixes that issue.


## 4.0.0 - 2019-07-01 [YANKED]

This release, while a major version release represents a merging of internal code repositories and does not introduce any changes to the input/output contracts [as currently documented](https://www.smarty.com/docs/cloud/us-street-api).

CHANGES:

- Local installations can now make use of up to 64 cores (previously the max was 8).
- Local installations should log slow status check durations less frequently (when applicable).
- Local installations no longer limit the size of request payloads. 
- Clients of local installations must now submit a `Content-Type` header with `application/json; charset=utf-8` for `JSON` payloads. Failure to do so will result in `HTTP 400 Malformed Request`.
    - One option would be to put the local installation behind your own proxy that performs an override in the case of certain common content types submitted by tools such as cURL (`x-www-formurlencoded` to `application/json; charset=utf-8`).

## 3.3.2 - 2019-06-24

- Updated internal dependencies. Incrementing the minor version number in this case was a mistake.


## 3.2.22 - 2019-04-30

CHANGES:

- Now compiled with Go 1.12 and Go modules.
- The service now runs in a docker image and has been fully migrated to geo-distributed kubernetes clusters.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 3.0.27 - 2019-03-26

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.26 - 2019-03-25

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.25 - 2019-03-08

CHANGES:
- Internal refactoring.


## 3.0.24 - 2019-03-06

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.

CHANGES:

- Overhauling module and deployment system. (No public-facing changes expected.)


## 3.0.23 - 2019-02-22

IMPROVEMENTS:

- Freeform inputs containing underscores (instead of spaces) will be sanitized and handled correctly.
- Updated all internal dependencies to latest versions.

BUG FIXES:

- Wireup race condition fixed in inner verification engine.


## 3.0.22 - 2018-11-29

IMPROVEMENTS:

- Latest internal dependencies


## 3.0.21 - 2018-11-29

BUG FIXES:

- Fixed county output in scenario categorized by a plus 4 code that crosses over a state line into a county with a FIPS code that matches the FIPS code of an unrelated county in the default state. Previously, the output contained county info pertaining to the unrelated county from the default state rather than the correct county in the adjoining state.
