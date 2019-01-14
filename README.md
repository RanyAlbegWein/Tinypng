A Bash script for shrinking PNG/JPEG files, using tinypng.com
===================

sha1sum: 0bf40e9721a3f280e803c039b6fccf58335cd2ca

<a href='https://ko-fi.com/E1E0B4X4' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi1.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

Dependencies
------------
Bash 4 ( and above ), and curl.

```
NAME
        tinypng - Shrink PNG/JPEGs using tinypng.com service.

SYNOPSIS
        tinypng [-dkph] -f FILE

DESCRIPTION
        Shrink PNG/JPEGs using tinypng.com service.
        
        On first execution, or if ~/.tinypng.apikey is not present, tinypng will ask for an API key.
        Obtain your API key from https://tinypng.com/developers, copy and paste it when prompted.

OPTIONS
        -f,--file FILE              Select a FILE to be shrinked.
        -d,--download DIRECTORY     Download all shrinked images to DIRECTORY.
        -k,--key API_KEY            Use API_KEY, instead of the one stored in ~/.tinypng.apikey.
        -p,--print                  When -d is being used, the URLs of the shrinked images are not being printed to stdout.
                                    Use this option to force printing even when using -d.
                                    Otherwise, this option is set implicitly.
        -- FILES                    Ignore any options to come.
                                    Everything after this option is considered a file.
        -h,--help                   Show this message and exit successfully.
            
EXAMPLES
        Shrink foo.jpg, bar.png, baz.png and print the result URLs to stdout.
        $ tinypng -f foo.jpg -f bar.png -f baz.png
            or
        $ tinypng -- foo.jpg bar.png baz.png
        Shrink foo.jpg, bar.png, baz.png and download the result images to tiny_pngs/ directory
        $ tinypng -d tiny_pngs/ -- foo.jpg bar.png baz.png
```

AUTHOR
-------

**Rany Albeg Wein**


LICENSE
--------
Use it as if you wrote it yourself.
