CrunchBang Window Manager Hacks
===============================

A script for adding hot corners and aero style window snapping to 
Openbox. Written for CrunchBang Linux (http://crunchbang.org/).

### Usage

Designed to be started automatically on login via Openbox's autostart 
file:

	# Start hotcorner and edge detection:
    cb-wmhacks --daemon &

Command line usage:

    cb-wmhacks: usage:
        --help          show this message and exit
        --kill          attempt to kill any running instances
        --daemon        run daemon and listen for cursor triggers
        --aero-left     attempt to snap active window to left of screen
        --aero-right    attempt to snap active window to right of screen

### Dependencies

* python
* python-xlib
* wmctrl

On Debian systems:

    sudo apt-get install python python-xlib wmctr

### Credits

The script is a hack of an existing script found on the Gentoo Wiki: 
http://en.gentoo-wiki.com/wiki/Fluxbox#Active_edges 

### License

WTFPL: http://sam.zoy.org/wtfpl/
