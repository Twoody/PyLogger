Author:
	Tanner.L.Woody@gmail.com
Date:
	2019-03-27

Setup [Unix/Linux]:
	Initial steps (only needed to be done once):
		1. mkdir ~/.pylog/
		2. cd ~/.pylog
		3. git clone https://github.com/Twoody/PyLogger.git
		4. mkdir logs
	In every python FILE:
		1. touch import_handler.py #IF NOT EXISTS
		2. from import_hanlder import *
	In every python MODULE:
		1. touch __init__.py #IF NOT EXISTS
		2. from MODULE import * #This goes in every file module is imported from..

	__init__.py and import_handler.py examples in /resources/examples/

	Setup path for `/USERS/tannerleewoody/` necessary modification in ~/.pylog/config.ini
	Setup path for `/USERS/tannerleewoody/` necessary modification in ~/.pylog/resources/examples/import_handler.py
		Mods should articulate a path you can `cd` too...

	Testing:
		1.	Make a few LOGGER.info('foo') calls in bar.py;
		2. python3 bar.py
		3. vim ~/.pylog/logs/main.log

Purpose:
	Properly configure a file for examples of:
		1. Logging to console.
		2. Logging to Files.
			A. Log files to `rotate`
			B. Rollover testing TODO
		3. Display of proper importing and configuration within a python exmaple

Functionality FOR NEW PROJECTS:
	In each __init__.py:
		import logging
		from logging.config import fileConfig
		fileConfig('/Users/tannerleewoody/.pylog/config.ini')
	
	AND THEN in config.py create declare the global `logger`
		LOGGER = logging.getLogger('test66')

	Finally, just import config.py into each class or into a import handler:
		from config.py import *
	

Further Readings:
	1. https://docs.python-guide.org/writing/logging/
	2. https://docs.python.org/3/library/logging.html
	3. 12 Factor App -- Logging
		A. https://12factor.net/
