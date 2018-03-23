# [SmartyList CLI](https://smartystreets.com/docs/plugins/smartylist/cli)


## 8.1.13 (December 18, 2017)

IMPROVEMENTS:

- Simplified internal build tasks (streamlined for go 1.9).


## 8.1.12 (December 18, 2017)

IMPROVEMENTS:

- Updated internal dependencies.


## 8.1.11 (August 28, 2017)

IMPROVEMENTS:

- Now using the [dep](https://github.com/golang/dep) tool for managing source code dependencies.


## 8.1.10 (August 15, 2017)

IMPROVEMENTS:

- Upgraded internal and open-source dependencies.


## 8.1.9 (July 31, 2017)

IMPROVEMENTS:

- Added new DPV footnotes supplied by US Street API and their definitions:

    "PB": "PO Box Street Address"
    "R7": "Phantom Address"


## Version 8.1.8 (May 11, 2017)

IMPROVEMENTS:

- Corrected the handling of the UTF-8 byte-order mark (https://en.wikipedia.org/wiki/Byte_order_mark). Without this fix, lists that contained a UTF-8 byte order mark and whose first column was the 'street' field could not be analyzed or processed because the required 'street' field was not recognized.


## Version 8.1.7 (May 4, 2017)

IMPROVEMENTS:

- Internal refactorings and improvements. May the 4th be with you...always.


## Version 8.1.6 (January 27, 2017)

FEATURES:

- Summary text is now "No Match - PO Box Only" for records whose `metadata.zip_type` is "PO Box" (`P`).


## Version 8.1.5 (December, 8, 2016)

IMPROVEMENTS:

- Internal optimizations.


## Version 8.1.4 (November 30, 2016)

IMPROVEMENTS:

- Internal optimizations.


## Version 8.1.3 (November 17, 2016)

IMPROVEMENTS:

- We've installed more verbose HTTP request tracing in error scenarios. This is in response to several recent
reports from users of intermittent timeouts and stalls and have been very tricky to reproduce. These seem to
be related to the network connections with our API servers, not the SmartyList tool itself. If your list
fails, please send the log file associated with that processing attempt to help us diagnose the problem.


## Version 8.1.2 (November 11, 2016)

BUG FIXES:

- Log file path can now be specified at the command line with the -log flag. We no longer display the -proxy and -base-url values in the list analysis if defaults are used.


## Version 8.1.1 (November 2, 2016)

IMPROVEMENTS:

- Increased HTTP timeout and retry parameters.


## Version 8.1.0 (October 31, 2016)

FEATURES:

- New command-line flag: -proxy (Allows lists to be processed via an organization's web proxy.)


## Version 8.0.4 (October 27, 2016)

UPGRADE NOTES:

- Failure by the smartylist tool to ascertain the latest version is grounds for early termination of the
program and a non-zero exit code. So there.


## Version 8.0.3 (October 17, 2016)

IMPROVEMENTS:

- Modified the output for addresses that completely fail verification that also have a "Unique" ZIP codes.


## Version 8.0.2 (October 10, 2016)

IMPROVEMENTS:

- Using the latest version of the smartystreets-go-sdk: 5.0.1 (which correctly buffers the request body for retry)


## Version 8.0.1 (October 6, 2016)

BUG FIXES:

- Prevent double url-encoding of auth-token



## Version 8.0.0 (October 4, 2016)

FEATURES:

1. JSON configuration files: Support for JSON config files is being dropped. The 'config'
command line flag will be removed. (For those wishing to avoid the auth-id and auth-token
values showing up in process lists those flags may be populated with the names of environment
variables containing the actual auth values.)

2. Schema: Support for the the 'zipcode' schema is being dropped. The 'address' schema is now
the only supported mode of operation. The 'schema' command line flag will be removed.

3. Batches: Support for customizing the number of concurrent bathes is being dropped as the
smartylist tool now uses the maximum number of batches by default. The 'batches' command line
flag will be removed.

4. Hostname: Support for customizing the hostname is being dropped. The 'hostname' command line
flag will be removed. (The base-url flag has been the preferred method of pointing to alternate
endpoints and will continue to be supported.)

5. Verbosity: The verbose and debug flags have been replaced by a single new flag: 'silent'. If
set, no output or prompts will be presented. The 'verbose' and 'debug' command line flags will
be removed.


In this version of smartylist, all configuration and options will be provided via the following
command-line flags (this is the same listing provided by 'smartylist -help'):

  -auth-id
    	The auth-id value (or name of environment variable) to use for API requests.
  -auth-token
    	The auth-token value (or name of environment variable) to use for API requests.
  -base-url
    	The base URL to use for API requests.
    	Unless you are pointing to an onsite API installation or a proxy the default value is appropriate.
    	Default: [https://api.smartystreets.com]
  -input
    	The path to the input file with records to verify/lookup. (REQUIRED)
  -log
    	The path to the diagnostic log file.
    	Default: [log_<datetime>.txt]
  -output
    	The path to the output file to create.
    	Default: [<input-filename>-output.<input-extension>]
  -silent
    	Squelch all diagnostic output and process list without confirmation prompt if possible.
  -version
    	Show the version and exit.


## Version 7.0.0 (August 29, 2016)

FEATURES:

- This version served as an intermediate version between 6.0.0 and 8.0.0. No new processing
behavior was released. The only change in this version was the addition of a series of
informational prompts warning the user of the changes listed below in version 8.0.0.
