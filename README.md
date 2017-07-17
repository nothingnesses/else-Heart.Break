# else-Heart.Break
Awesome code for items in the game else Heart.Break().

# Purpose
The codes are pretty well documented and should easy enough to follow so reading those should give a pretty good gist of what they do. In general though:

The Drink code allows any drink coded with it when drunk to:
* Teleport anyone or anything to anyone or anything or anywhere.
* Find the name or position of anyone or anything in the room or entire world, copy them if required.
* Find the name of any room and copy it if required.
* Change the weather.
* Do basic maintenance - finance Sebastian, register money to Wellspringer so you keep your job, alleviate sleepiness, drunkenness, etc.
* Self-replenish.

The Key code allows any key coded with it when used on any door to toggle the door using values obtained from different bruteforce algorithms of choice, useful for when a second modifier has not yet been obtained.

The Modifier code allows any modifier coded with it to hack any hackable object as well as lock or unlock any door hacked with it.

# Notes
The scripts for Key and Drink's "Search for thing" and "Search for room" functions have a long execution duration and will inevitably stop after 60 seconds. To prevent this, pause the game when running them as scripts continue to run (and at a faster rate) even when the game is paused.

Additionally, to speed up "Search for thing" and "Search for room" you can obtain a screwdriver, change its code to:

```
SetMhz(500)
SetMaxTime(-2)
```

then use it on PoliceOfficeInterior_MinistryOfficeWorkstationComputer_1 and PoliceOfficeInterior_LargeRecorder_LargeRecorder_1. If you don't know which ones these are, you can use an extractor on the computers in the Police Station or just use the screwdriver on all the computers to make sure they were done.

When copy is turned on, and especially for the "Search for thing" and "Search for room" functions, do note that even though everything will be copied, they will only be copied one at a time so it may be a good idea to have a text editor outside of the game ready to paste the contents of the clipboard in. Maybe use some macro program to automate the pasting process.

Happy hacking!
