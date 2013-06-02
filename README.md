# Sublime Text package for Rust

## About

This package supports current rust at the time of writing;
it makes no attempt at backwards compatibility.
This is intended to be a feature - if keywords no longer highlight,
it means that the keyword has changed or will soon

## Installation

Install the Package Control package if you haven't got it yet. Package 
Control is the best way to install packages for Sublime Text. See 
http://wbond.net/sublime_packages/package_control/installation for 
instructions.

Open the palette (`control+shift+P` or `command+shift+P`) in Sublime Text
and select `Package Control: Install Package` and then select `Rust` from 
the list. That's it.

## Development

The files are written in the JSON format supported by the Sublime Text 
package [AAAPackageDev](https://github.com/SublimeText/AAAPackageDev), 
because the format is much easier to read / edit
than the xml based plist format.

So install that package and then work on the .JSON-* files. There is a 
build system that comes with that package, so if everything is set up
right, you should just be able to trigger the build (F7) and get the
corresponding .tmLanguage / .tmPreferences files. It will also display
errors if you have not formatted the file correctly.

One impact of using this indirect format is that you usually have to double 
escape anything in the match patterns, ie, "\\(" has to be "\\\\(" as otherwise
it will try to interpret '\\(' as a JSON escape code (which doesn't exist).

## Credits

Created 2012 by [Daniel Patterson](mailto:dbp@riseup.net), as a near complete from 
scratch rewrite of a package by [Felix Martini](https://github.com/fmartini).

Derived primarily from the Vim syntax file, maintained by
[Patrick Walton](https://github.com/pcwalton) and
[Ben Blum](https://github.com/bblum)

With a little help from the (now very outdated) TextMate rust mode written 
by [Tom Ellis](https://github.com/tomgrohl).

## License

This package is licensed under the MIT License.
