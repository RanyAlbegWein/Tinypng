A Bash script for shrinking PNG files, using tinypng.com
===================

Dependencies
------------
Bash 4 ( and above ), and curl.

```
NAME
        tinypng - Shrink PNGs using tinypng.com service.

SYNOPSIS
        tinypng [-dkph] -f FILE

DESCRIPTION
        Shrink PNGs using tinypng.com service.
        
        On first execution, or if ~/.tinypng.apikey is not present, tinypng will ask for an API key.
        Obtain your API key from https://tinypng.com/developers, copy and paste it when prompted.

OPTIONS
        -f,--file FILE              Select a FILE to be shrinked.
        -d,--download DIRECTORY     Download all shrinked PNGs to DIRECTORY.
        -k,--key API_KEY            Use API_KEY, instead of the one stored in ~/.tinypng.apikey.
        -p,--print                  When -d is being used, the URLs of the shrinked PNGs are not being printed to stdout.
                                    Use this option to force printing even when using -d.
                                    Otherwise, this option is set implicitly.
        -- FILES                    Ignore any options to come.
                                    Everything after this option is considered a file.
        -h,--help                   Show this message and exit successfully.
            
EXAMPLES
        Shrink foo.png, bar.png, baz.png and print the result URLs to stdout.
        $ tinypng -f foo.png -f bar.png -f baz.png
            or
        $ tinypng -- foo.png bar.png baz.png
        Shrink foo.png, bar.png, baz.png and download the result PNGs to tiny_pngs/ directory
        $ tinypng -d tiny_pngs/ -- foo.png bar.png baz.png
```

AUTHOR
-------

**Rany Albeg Wein**


LICENSE
--------
Copyright [2016] [Rany Albeg Wein]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
