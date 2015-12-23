Heroku buildpack: FFMpeg
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [ffmpeg](http://www.ffmpeg.org/) in your project.  
It doesn't do anything else, so to actually compile your app you should use [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) to combine it with a real buildpack.

Usage
-----

To use this buildpack add it to the start of your buildpacks list with:

    $ heroku buildpacks:add --index 1 https://github.com/tastemade/heroku-buildpack-ffmpeg --app <app-name>

Confirm that it is in the list with:

    $ heroku buildpacks --app <app-name>

    === <app-name> Buildpack URLs
    1. https://github.com/tastemade/heroku-buildpack-ffmpeg
    2. heroku/ruby

Hacking
-------
If you want to use your own ffmpeg binary, fork and rewrite following line.

https://github.com/megaphone/heroku-buildpack-ffmpeg/blob/master/bin/compile#L10
