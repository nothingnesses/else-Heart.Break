# else-Heart.Break
Awesome code for items in the game [else Heart.Break()](http://elseheartbreak.com/ "else Heart.Break() Homepage").

# Purpose
The codes are pretty well-commented so reading the comments should give a pretty good gist of what the codes do. There is a separate Drink Manual to be used as a guide when using the Drink code. In general though:

* The Drink code allows any drink coded with it when drunk to:
    * Teleport anyone or anything to anyone or anything or anyplace.
    * Find the position of anything in the world, copy the results if required.
    * Get the names of everything and everyone in the room and copy the results if required (not working as intended).
    * Find the name of anyone or anything in the world, copy the results and/or teleport anything or anyone to them or teleport them to anything or anyone or anyplace if required.
    * Find the name of any room and copy the results and/or teleport anything or anyone to them if required.
    * Cause anyone to try to interact with anyone or anything.
    * Knock out and/or zap anyone.
    * Change the weather.
    * Do basic maintenance - finance Sebastian, register money to Wellspringer so you keep your job, alleviate sleepiness, drunkenness, etc.
    * Self-replenish.

* The Key code allows any key coded with it when used on any door to toggle the door using values from a list (which contains all(?) the door values as of version 1.0.9 of the game) or values obtained from different bruteforce algorithms of choice. Useful for when a second modifier has not yet been obtained.

* The Modifier code allows any modifier coded with it to hack any hackable object as well as toggle the lock state of any door hacked with it, kind of (toggle state is dependent on a memory value stored in a computer and is independent to each door).

* The Computer code allows a computer (which has the Floppy API enabled) coded with it to clear the currently held floppy then write a list containing the names of everything in the world, along with the names of the rooms containing them, and their coordinates into the floppy.

# Notes
* The codes (bar the Computer code) accept variables located near the top which should be edited as required to alter the behaviour of the items. As mentioned, reading the comments should help.

* The codes for the Computer, Key, and Drink (specifically, the latter's "Search for thing" and "Search for room" functions) have a long execution duration and will inevitably stop after 60 seconds. To prevent this, pause the game when running them because they continue to run (and at a faster rate) even when the game is paused.

* Additionally, to speed up the Computer code and the Drink code's "Search for thing" and "Search for room" functions you can obtain a screwdriver, change its code to:

```
SetMhz(500)
SetMaxTime(-2)
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;then use it on the computer you have modified with the Computer code, on &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;PoliceOfficeInterior_MinistryOfficeWorkstationComputer_1, and on &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;PoliceOfficeInterior_LargeRecorder_LargeRecorder_1. If you don't know which ones these are, you can use an
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;extractor on computers to see which ones have those names.

* Additionally, because the Computer code requires a computer with the Floppy API enabled, you can use a screwdriver containing the code:

```
EnableAPI("floppy")
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;on any computer without the API enabled to enable it such that floppies can be used with it.

* When the Drink code's "copy" variable is set to 1, and especially for the "Search for thing" and "Search for room" functions, do note that even though everything will be copied, they will only be copied one at a time so it may be a good idea to have a text editor outside of the game ready to paste the contents of the clipboard in. Maybe use some macro program to automate the pasting process.

Thanks TinTans for your help, insights, and code.

Happy hacking!
