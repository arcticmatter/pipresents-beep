PI PRESENTS  - Version 1.4.4
============================

This repository contains an unofficial and independent fork of Pi Presents as found here https://github.com/KenT2/pipresents-beep/

Note that the original licence still applies.

Pi Presents is a toolkit for producing interactive multimedia applications.

Pi Presents needs to be configured for your application. This is mainly achieved using a graphical editor. There are numerous tutorial examples and a comprehensive manual.

For a detailed list of applications and features see here:

          https://pipresents.wordpress.com/features/



Installing Pi Presents Beep
===============================

The full manual in English is here https://github.com/arcticmatter/pipresents-beep/blob/master/manual.pdf. It will be downloaded with Pi Presents.


Requirements
-------------

	* must use the latest version of Raspbian Buster with Desktop (not the Lite version)
	* must be run from the PIXEL desktop.
	* must be installed and run from user Pi
	* must have Python 3 installed (which Raspbian does)


Set the GPU Memory size to 256MB
---------------------------------
Using the Raspbian menu preferences>raspberry pi configuration>performance, increase the GPU Memory to 256.


Ensure Raspbian is up to date.
-------------------------------
Pi Presents MUST have the latest version of omxplayer and of Raspbian, get this by

         sudo apt update && apt upgrade


Install required packages 
-----------------------------
         sudo apt install python3-pil.imagetk unclutter mplayer python3-pexpect chromium-chromedriver
         
         sudo pip3 install selenium
         sudo pip3 install python-vlc

Install optional packages
------------------------------
         sudo pip3 install evdev  (if you are using the input device I/O plugin)
         sudo apt install mpg123 (for .mp3 beeps)
         sudo apt install uzbl   (for legacy uzbl browser)

	   
Download Pi Presents Beep
----------------------------

From a terminal window open in your home directory type:

         wget https://github.com/arcticmatter/pipresents-beep/tarball/master -O - | tar xz     # -O is not null...

There should now be a directory 'arcticmatter-pipresents-beep-xxxx' in your /home/pi directory. Copy or rename the directory to pipresents

Run Pi Presents to check the installation is successful. From a terminal window opened in the home directory type:

         python3 /home/pi/pipresents/pipresents.py

You will see a window with an error message which is because you have no profiles.Click OK to exit Pi Presents.


Download and try an Example Profile
-----------------------------------

Examples are in the github repository pipresents-beep-examples.

Open a terminal window in your home directory and type:

         wget https://github.com/arcticmatter/pipresents-beep-examples/tarball/master -O - | tar xz

There should now be a directory 'arcticmatter-pipresents-beep-examples-xxxx' in the /home/pi directory. Open the directory and move the 'pp_home' directory and its contents to the /home/pi directory.

From the terminal window type:

         python3 /home/pi/pipresents/pipresents.py -p pp_mediashow_1p4
		 
to see a repeating multimedia show

Exit this with CTRL-BREAK or closing the window, then:

          python3 /home/pi/pipresents/pipresents.py -p pp_mediashow_1p4 -f -b
		  
to display full screen and to disable screen blanking


Now read the manual to try other examples.



Getting examples.
-----------------

Examples are in the github repository pipresents-beep-examples.

Rename the existing pp_home directory to old_pp_home.

Open a terminal window in your home directory and type:

         wget https://github.com/arcticmatter/pipresents-beep-examples/tarball/master -O - | tar xz

There should now be a directory 'arcticmatter-pipresents-beep-examples-xxxx' in the /home/pi directory.

Open the directory and move the 'pp_home' directory and its contents to the /home/pi directory.



Licence
=======

Copyright (c) 2013, Ken Thompson.

Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.
