# tintin-helper
A set of helper modules for tintin users.

Two of the most common questions I get at Legends of Kallisti about tintin++ are how to set up mapping,
and how to enable a comms log.  I started working on a modloader for tintin++, and this is the result.

Most of it will work on any MUD, and we'll either leave instructions to turn off the Kallisti modules,
or make the default MUD-agnostic and show how to enable Kallisti.

I've been trying to keep it safe for tt++ on linux, and wintin on Windows 10, and so far that seems
to be working.

This is not yet production ready, but please feel free to test and provide feedback.  It does require
tt++/wintin 2.02.11 or relatively close in a few modules.

What works today:
* Basic layouts:
  full - panel at top, right and left, bottom status bar, input line
  right - panel at top and right, bottom status bar, input line
  simple - input line only
* Mapping, with permanent onscreen map in full and right layouts
* Basic communications trapping, top panel display, and separate session with history
* Login and account management for Legends of Kallisti
* Support for custom/individual tintin scripts
* Kallisti module supports connection, and password management (forget after use)
* Automatic subscription to all MSDP values, and event firing when they update
* Registration status of loaded modules with error handling
* In-game help command for modules
* Basic syslog/info display support
* data tile placement in the panels, and samples, like Kallisti-specifc zone and group info

What's coming next:
* better logging controls
* more tile options and commands

Screenshots:
![Layout "full"](/screenshots/layout_full.jpg?raw=true "Comms bar, bottom bar, right and left panels")
![Layout "right"](/screenshots/layout_right.jpg?raw=true "Comms bar, bottom bar, right panel only")
![Layout "simple"](/screenshots/layout_simple.jpg?raw=true "Simple input line split")
![Help and list_modules](/screenshots/help_and_list.jpg?raw=true "Help and list_modules sample")
