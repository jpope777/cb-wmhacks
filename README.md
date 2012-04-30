CrunchBang Window Manager Hacks
===============================

Scripts for adding hot corners and aero style window snapping to 
Openbox. Written for CrunchBang Linux (http://crunchbang.org/).

### cb-hotcorner usage:

This script is designed to be started automatically on login via 
Openbox's autostart file:

	# Start hotcorner detection:
    cb-hotcorners --daemon &

Once started, the script will detect when the mouse cursor enters 
the corners of your screen. If the corner has an associated command, 
it will get executed.

#### Command line usage:

    cb-hotcorners: usage:
        --help          show this message and exit
        --kill          attempt to kill any running instances
        --daemon        run daemon and listen for cursor triggers

#### Customising commands:

On first use, a config file will be created 
`~/.config/cb-hotcorners/cb-hotcornersrc`. The file should be 
self-explanatory.

### cb-aerosnap usage:

This script is designed to be called via Openbox keyboard shortucts. 
Edit Openbox's rc.xml file to add new shortcuts. Example shortcuts to
bind snapping to Super+Alt+Left/Right key combinations:

    <keybind key="W-A-Left">
        <action name="Execute">
            <command>cb-aerosnap --left</command>
        </action>
    </keybind>
    <keybind key="W-A-Right">
        <action name="Execute">
            <command>cb-aerosnap --right</command>
        </action>
    </keybind>

#### Command line usage:

    cb-aerosnap: usage:
        --help          show this message and exit
        --left          attempt to snap active window to left of screen
        --right         attempt to snap active window to right of screen

### Dependencies

* python
* python-xlib
* wmctrl
* xdotool (>=2.20110530)

On CrunchBang systems:

    sudo apt-get update && sudo apt-get install python python-xlib wmctrl xdotool
    
### Packages

On CrunchBang systems, these scripts are available for both Statler and 
Waldorf branches via their package repositories. Waldorf releases include 
the package by default.

    sudo apt-get update && sudo apt-get install cb-wmhacks

### License

WTFPL: http://sam.zoy.org/wtfpl/
