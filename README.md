# else-Heart.Break
Awesome code for items in the game [else Heart.Break()](http://elseheartbreak.com/ "else Heart.Break() Homepage").

#	Purpose
The codes are pretty well-commented so reading the comments should give a pretty good gist of what the codes do. There is a separate man drink.sprak to be used as a guide when using drink.sprak. In general though:

* screwdriver.sprak allows screwdrivers coded with it, when used on computers, to set their execution times to infinite, their clockspeed to 500MHz, and activates the "arcade","door", "floppy", "internet", "memory" APIs on them.

* server.sprak allows computers coded by it to connect to other objects and provide functions to other objects connected to it.

* drink.sprak and drink_nopc.sprak allows any drink coded with it when drunk to:
    * Lock/unlock all the doors near/not near Sebastian.
    * Teleport anyone or anything to anyone or anything or anyplace.
    * Find the position of anything in the world, copy the results if required.
    * Get the names of everything and everyone in the room and copy the results if required.
    * Find the name of one or more person or thing in the world at a time, copy the results if required.
    * Find the name of one or more room at a time and copy the results if required.
    * Cause one or more person at a time to interact with anyone or anything.
    * Knock out and/or zap one or more person at a time.
    * Knock out and/or zap other people in the same room as the drinker.
    * Change the weather.
    * Do basic maintenance - finance Sebastian, register money to Wellspringer so you keep your job, alleviate sleepiness, drunkenness, etc. 

* modifier.sprak and modifier_nopc.sprak allows any modifier coded with it to hack any hackable object as well as toggle the lock state of any door hacked with it, kind of (toggle state is dependent on a memory value stored in a computer which is separate for each door, i.e., the lock state of each door is independent of one another).

* key.sprak allows any key coded with it when used on any door to toggle the door using values from a list (which contains all(?) the door values as of version 1.0.9 of the game) or values obtained from different bruteforce algorithms of choice. Useful for when a second modifier has not yet been obtained.

#	Notes
* The nopc variants of the some of the codes don't require a computer coded with server.sprak, but are larger in size and run slower than their standard counterparts.

* The codes accept variables located near the top which should be edited as required to alter the behaviour of the items. As mentioned, reading the comments should help.

* server.sprak, key.sprak, and drink.sprak (specifically, the latter's search_for_things and search_for_rooms functions) have long execution durations and may stop after a while. To prevent this, pause the game when running them because they continue to run (and at a faster rate) even when the game is paused.

* Additionally, to speed up server.sprak, drink.sprak and modifier.sprak and prevent them from stopping, you can obtain a screwdriver and code it with screwdriver.sprak and then use it on the computer.
