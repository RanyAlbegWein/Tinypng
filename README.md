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
Copyright (C) 2014 Rany Albeg Wein - rany.albeg@gmail.com

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

