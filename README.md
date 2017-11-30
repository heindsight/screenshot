# Screenshot

A script to capture X11 screenshots using the GraphicsMagick (or ImageMagick)
`capture` command.

## Requirements

* [GraphicsMagick](http://www.graphicsmagick.org/) or
  [ImageMagick](http://www.imagemagick.org)  is required for capturing
  screenshots.
* [libnotify](https://git.gnome.org/browse/libnotify) is required for
  displaying notifications

## Installation

To install, simply copy the `screenshot` script to a directory on your path.
For example:

    cp ~/git/screenshot/screenshot ~/bin

Alternatively you can create a symlink to the script from a directory on your
path. For example:

    ln -s ~/git/screenshot ~/bin/

## Usage

To capture the entire screen, use

    screenshot output.png

To capture the active window, use

    screenshot -a output.png

To interactively select a rectangular area to capture, use

    screenshot -i output.png

If no filename is provided, a default filename will be chosen. Default
filenames consist of the window instance name (the first part of the `WM_CLASS`
property as output by `xprop`) and the current date and time. When capturing
the entire screen, the window name `root` is used. In interactive mode, the
default filename consists of the word `screenshot` and the current date and
time. E.g `xterm-2017-11-29T23:10:20.868+00:00.png` or
`root-2017-11-29T23:11:00.977+00:00.png` or
`screenshot-2017-11-29T23:11:37.002+00:00.png`.

The `-n` option can be used to display a notification after capturing the
screenshot:

    screenshot -a -n
