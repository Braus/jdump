J!Dump %%VERSION%% README
===============================
(%%TODAY%%)

Advanced print_r and var_dump replacer with object tree display.

Follow @mathiasverraes on Twitter for updates.

Features
--------

This utility makes life easy for developers and template designers. You use it to 
see what's inside a variable, an array or an object. Instead of using print_r() or 
var_dump(), you can now use dump(). This will open a popup window with a nice expandable 
DHTML tree, showing the contents of the variable. It will even show a list of available 
methods for each object. You have to see it to believe it! You can use dump() in your 
extensions, in the core, in libraries and even in templates.

**Warning!** This component is only meant to be used on development test sites, NOT 
in live or production environments. If you must use it on a live site, don't do 
stupid things like dump($password) !


Installation
------------

Install both the component and the plugin. Make sure the plugin is published. But you probably figured that out already.

If you don't want the dump popup window to appear automatically, you can disable it in the configuration. To display the dump window manually:

- **Administrator**: Go to Components -> J!Dump and click Popup.
- **Site**: Make a new menu item for J!Dump. Set it to 'Open in New Window'


Using J!Dump
------------

Anywhere in your code, type:

::
	
	dump($variable, 'Variable Name');

Simple huh? 'Variable Name' is optional and can be anything you like. If you use a lot of dumps, you'll want to use some descriptive names.

Shortcuts
---------

::
	
	// Displays a whole bunch of system information.
	dumpSysinfo();


::
	
	// Use inside a template's index.php to dump the parameters.
	dumpTemplate($this);


::
	
	// Displays a custom message. Very handy to check if a function or a loop is executed etc...
	dumpMessage('Your message');


::
	
	// Displays the backtrace.
	dumpTrace();
	

Notes
-----

You can't use dump() in system plugins that are run before the J!Dump plugin is run, so it is best to use ordering in the plugin manager to put J!Dump upfront.


Contributors
-------------

- Mathias Verraes (Lead)
- Jens-Christian Skibakk
- Tom Fuller

Thanks to everybody who provided patches!

License
-------

J!Dump is licensed as GNU/GPL v2.

Credits
-------

This component includes Folder Tree Static by Alf Magne Kalleland. It is released under LGPL and can be found at http://www.dhtmlgoodies.com/