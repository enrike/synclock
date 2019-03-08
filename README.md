# synclock by ixi-audio.net
A chronometer that runs in sync in many devices at the same time (android and pcs). Developed in PureData

License GPL

Synclock is a PD patch with a chronometer that runs in sync in many devices at the same time. The devices must be in the same network (firewalls might interfiere). It starts at -10 secs and gets up to 59:59


requires: 
- computer: Pure Data and the libraries SyncJam and Pddroidparty
https://github.com/chr15m/SyncJams
http://www.droidparty.net/ 

- android: install PdDroidparty apk (http://www.droidparty.net) and zip up the folder with your patch in it, renaming the file extension from .zip to .dpz. Send a .dpz file to somebody, then PdDroidParty will launch and run the patch..

usage:
- in a computer: just open droidparty_main.pd in Pure Data
- in a android device: zip the droidparty_main.pd file and rename the zip with extension .dpz then try to open it. PdDroidparty should open the patch. To start the chronometer press the orange button and to restart the timer press the red button.

issues:
sometimes it takes a while for new devices that join to get in sync with the others
