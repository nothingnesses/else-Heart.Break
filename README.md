# else-Heart.Break
Awesome code for items in the game else Heart.Break().

# Notes
The scripts for Key and Drink's "Search for thing" and "Search for room" functions have a long execution duration and will inevitably stop after 60 seconds. To prevent this, obtain a screwdriver, change its code to:

SetMhz(500)

SetMaxTime(-2)

then use it on PoliceOfficeInterior_MinistryOfficeWorkstationComputer_1 and PoliceOfficeInterior_LargeRecorder_LargeRecorder_1. If you don't know which ones these are, you can use an extractor on the computers in the Police Station or just use the screwdriver on all the computers to make sure they were done.

Also, scripts continue to run (and at a faster rate) even when the game is paused, so it is a good idea to do so when using them.
