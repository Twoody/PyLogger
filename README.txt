Author:
	Tanner.L.Woody@gmail.com
Date:
	2019-03-27

Purpose:
	Essentially, in every __init__.py place:
		import logging
		logging.getLogger(__name__).addHandler(logging.NullHandler())

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
