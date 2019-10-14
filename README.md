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
* Read from pipe
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
	* [__Curl__](https://curl.haxx.se) for get Search file from Web
	* [__Dmenu__](https://tools.suckless.org/dmenu/) For Url select

2. Set up [Urlgate]:

	``` bash
	git clone https://gitlab.com/zakariaGatter/urlgate.git ~/brash
	mkdir -p ~/.local/bin
	cp ~/brash/bin/urlgate ~/.local/bin
	chmod +x ~/.local/bin/urlgate
	```

## Using Urlgate

```
URLGATE
Write by Zakaria Gatter (zakaria.gatter@gmail.com)

Extract URLs from a text file in bure bash

urlgate [OPTS]

OPTS :
	-c|--curl 	: Download website tp Extract URLs from
	-f|--file 	: Give file to Extract URLs from
	-g|--grep 	: Search for URLs with grep
	-d|--dmenu 	: Use dmenu for URL select
	-e|--exec 	: Run Command on Selected URL

NOTE :
	- You can pipe out from external Commands or Programs
		ex : cat /path/to/file | urlgate -d

	- You can change dmenu options with "_DMENU_OPTS_" variable
		ex : _DMENU_OPTS_="-p "URL SELECT :" -i -nb black -nf white" && urlgate -f /path/to/file -d

	- You can change default search REGEX options with "_URLGATE_REGEX_" variable
		ex : _URLGATE_REGEX_="http?://[^ ]+" && urlgate -f /path/to/file

	- You can change default grep options with "_GREP_OPTS_" variable
		ex : _GREP_OPTS_="-Ei" && urlgate -f /path/to/file -g "youtube.com
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


[Urlgate]:http://gitlab.com/zakariagatter/urlgate
