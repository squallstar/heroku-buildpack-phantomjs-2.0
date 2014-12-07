Heroku buildpack: PhantomJS 2.0
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) of [PhantomJS 2.0](http://phantomjs.org).

Usage
-----

Requires a [Cedar-14](https://devcenter.heroku.com/articles/cedar-14-migration) stack.
Migrate to this stack prior to running.

Also required is the [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi)
and the [heroku-buildpack-apt](https://github.com/ddollar/heroku-buildpack-apt)


Example usage:

```shell
$ heroku create --stack cedar-14 --buildpack https://github.com/ddollar/heroku-buildpack-multi
$ echo "https://github.com/ddollar/heroku-buildpack-apt" >> .buildpacks
$ echo "https://github.com/srbartlett/heroku-buildpack-phantomjs-2.0.git" >> .buildpacks
$ echo "libicu-dev" >> Aptfile

$ git push heroku master
```
