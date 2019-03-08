# synclock 
by ixi-audio.net
A chronometer that runs in sync in many devices at the same time (android and pcs). Developed in PureData

License GPL

Synclock is an atempt to create a chronometer that runs in sync in many devices at the same time. The devices must be in the same network (firewalls might interfiere). It starts at -10 secs and gets up to 59:59. It is programmed in PD.

There are two versions:

- synclock: This version a device acts as a master (press the master connect button) and broadcasts the time to the other devices in the network. Any device can join at any time and it will be automatically in sync. This version borrows some code from the nice SyncJams library (https://github.com/chr15m/SyncJams).

- synclock_jams: It uses the SyncJams to syncronise all devices in the network. When a new device joins the chronometer must be reset.



Usage and requirements: 

- computer: 
It needs Pure Data and Pddroidparty http://www.droidparty.net/ 
The second version also needs SyncJams https://github.com/chr15m/SyncJams
1. Just open droidparty_main.pd and press the orange button.

- android: 
1. Install the PdDroidparty apk (http://www.droidparty.net) 
2. Copy the SyncJams patches in a subfolder called "syncjams" in the synclock main patch. Get the patches here https://github.com/chr15m/SyncJams/tree/master/pure-data
3. Zip up the Synclock (with the symjams subfolder included) with a zip program (you might need to remove the .git folder before zipping)
4. Rename the file extension from .zip to .dpz
4. Send a .dpz file to the any device via email, whatsapp ... 
5. Try to open it. PdDroidParty will launch and run the patch.
6. When all devices are ready press the orange button in one of them.
6. From now on just run PdDroidParty



issues:
sometimes it takes a while for new devices that join to get in sync with the others
