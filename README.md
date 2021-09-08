
A `bash` script for shrinking _PNG/JPEGs_  with [TinyPNG](https://tinypng.com/)
===================

sha1sum: 6a4c4d06cec19b44c8b5512a1136468a7b7dce71

<a href='https://ko-fi.com/E1E0B4X4' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi1.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

### Dependencies
* `bash` 4+
* `curl`

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
-o,--overwrite              When -d is being used, overwrite the source images with the downloaded ones.
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

### EXAMPLES
Shrink *foo.jpg*, *bar.png*, *baz.png* and print the result URLs to stdout.

    $ tinypng -f foo.jpg -f bar.png -f baz.png
or

    $ tinypng -- foo.jpg bar.png baz.png

Shrink _foo.jpg_, _bar.png_, _baz.png_ and download the result images to _tiny_pngs/_ directory

    $ tinypng -d tiny_pngs/ -- foo.jpg bar.png baz.png

### With `find`:

Every argument after the `--` option is considered a file, therefore you might want to combine it with `find`'s `{} +` if available.

Find all _PNG/JPEG_ under _images/_, shrink and download results to _tiny_pngs/_

`find images/ -type f \( -name '*.png' -o -name '*.jpg' \) -print -exec tinypng -d tiny_pngs/ -- {} +`

For more information on using `find`, refer to [UsingFind](https://mywiki.wooledge.org/UsingFind)

## Thank you guys!

* [Wolf](https://github.com/AdAvAn)
* [Di](https://github.com/AdAvAn)

### LICENSE
Use it as if you wrote it yourself.
