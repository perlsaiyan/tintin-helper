Everything in this directory should be for use with the modloader routine.  If support files are needed, they
should live in either a subdirectory with the same name as the module, or in $db/ or $player/ or other
appropriate directory.

Modloader is still under active development, and the format is still changing, but module.stub contains a sample
module.  Replace "modname" with the actual module name, including the filename.  Do not wrap in a class (modloader
handles this for you), but may contain classes in them if needed (I think, needs testing).  They must/may include
some support aliases:

* modname-register : alias called after reading in the file to the class
* modname-unregister: alias called before killing the associated class (cleanup routines)

Some support vars may be set as well:
* modname-description : short description of the module, used in list_modules
* modname-help : what is displayed for "help modname"

For the modname-register alias, you must have register_module modname on success.  On failure, you should call
fail_module with appropriate details or syslog an error and clean up appropriately.

```
#nop --
#nop Class Definitions
#nop --

#var modname-description {description}
#var modname-help {help file}

#nop --
#nop Modloader Stuff
#nop --

#alias modname-register {
	#if {@isloaded{modloader}} {
		register_module modname
	} {
		fail_module modname unknown reason
	}
}
```
