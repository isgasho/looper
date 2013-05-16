# Looper

Looper is a development tool for the [Go Programming Language][go]. It automatically runs your tests and hot compiles your code when it detects file system changes.

## Status

[![Build Status](https://travis-ci.org/gophertown/looper.png?branch=master)](https://travis-ci.org/gophertown/looper)

This is an *early alpha*. There is still quite a lot to do (Hot Compiles, Growl notifications, and interactions for profiling, benchmarking, etc.). Also, it has only been tested on Mac OS X 10.8.

See the public [Trello board](https://trello.com/b/VvblYiSE) for the Roadmap.

## Get Going

If you are on OS X, you need to first install GNU Readline via [Homebrew](http://mxcl.github.com/homebrew/):

``` console
$ brew install readline
```

To install Looper, or to update your installation, run:

``` console
$ go get -u github.com/gophertown/looper
```

Then run `looper` in your project folder:

``` console
$ looper
Looper 0.1.2 is watching your files
Type help for help.

Watching path ./
```

## Autotest

By convention, [Go][] code has a *counterpart* test file in the same folder. When Looper detects a change to your production code or the test itself, it will run the appropriate test.

If you have a `suite_test.go` in the same folder, Looper will include it in every test run. Use it for a Suite definition ([Gocheck][], [PrettyTest][pat]), additional Checkers, or other testing helpers.

## Hot Compiles

...to be determined...

## Interactions

* `a`, `all`, `↩`: Run all tests.
* `h`, `help`: Show help.
* `e`, `exit`: Quit Looper

## Thanks

Inspired by Andrea Fazzi's [PrettyAutoTest][pat]. Special thanks to Chris Howey for the [fsnotify][] package.

[go]: http://golang.org/
[fsnotify]: https://github.com/howeyc/fsnotify
[pat]: https://github.com/remogatto/prettytest
[devweb]: http://code.google.com/p/rsc/source/browse/devweb/
[shotgun]: https://rubygems.org/gems/shotgun
[Gocheck]: http://labix.org/gocheck

