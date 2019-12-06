# UrlGate

## Table of Contents

- [About](#about)
- [Quick Start](#quick-start)
- [Using Urlgate](#using-zshing)
- [TODO](#todo)

## About

[Urlgate] Extract URLS from a text file in bure bash

[Urlgate] allows you to...

* Get lis of URLS
* Read from pipeline
* Grep to special URLS
* Curl text file from the web
* Use dmenu for Selection
* Exec a command after select

[Urlgate] automatically...

* Check if the file exist
* Check all possible user mistakes

[Urlgate] is undergoing an interface change, please stay up to date to get latest changes.

## Quick Start

1. Introduction:

   Installation requires :
	* [Curl](https://curl.haxx.se)
	* [Dmenu](https://tools.suckless.org/dmenu/)
    * [Coreutils]()

2. Set up [Urlgate]:

	``` bash
	git clone https://gitlab.com/zakariaGatter/urlgate.git ~/brash
	mkdir -p ~/.local/bin
	cp ~/brash/bin/urlgate ~/.local/bin
	chmod +x ~/.local/bin/urlgate
	```

## Using Urlgate

```
URLGATE Extract URLs from a text file
Usage: urlgate [OPTIONS] ... [FILE] ...
   Or: [CMD] | urlgate [OPTIONS]

OPTIONS
 -f <file> : Extract URLs from file
 -c <url>  : Extract URLs from the web
 -C <flgs> : Pass arguments to curl
 -l        : List All Extracted URLs
 -g <text> : Use only URLs that match TEXT
 -G <flgs> : Pass arguments to grep
 -s        : Show Selection Menu
 -d <file> : Dmenu command to use
 -D <flgs> : Pass arguments to dmenu
 -e <file> : Exec command or script to use [%u = URL]
 -r <regx> : REGEX regular expressions to use
 -h        : Display this help text and exit

VARIABLES
 URLGATE_GREP_FLG   Pass arguments to grep
 URLGATE_DMENU_CMD  Dmenu command to use
 URLGATE_DMENU_FLG  Pass arguments to dmenu
 URLGATE_CURL_FLG   Pass arguments to curl
 URLGATE_EXEC       Exec command or script to use
 URLGATE_REGEX      REGEX regular expressions to use
```

## TODO
[Urlgate] is a work in progress, so any ideas and patches are appreciated.

* [X] List URLs from file
* [X] Use Curl for web file
* [X] Read from STDIN
* [X] Grep URL list
* [X] Use Dmenu to select
* [X] Exec command after select
* [X] Mofidy dmenu, grep, and search options


[Urlgate]:http://github.com/zakariagatter/urlgate
