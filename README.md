# Screenshot

A script to capture X11 screenshots using the ImageMagick `capture` command.

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
