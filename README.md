# synclock a0.1

by ixi-audio.net 2019/03/10


A chronometer that runs in sync in many devices at the same time (android and pcs). Developed in PureData

License GPL

Synclock is an atempt to create a chronometer that runs in sync in many devices at the same time. The devices must be in the same network (firewalls might interfiere). It starts at -10 secs and gets up to 59:59. It is programmed in PD.

There are two versions:

- synclock: It uses the SyncJams library (https://github.com/chr15m/SyncJams) to syncronise all devices in the local network. The time is shared between all devices in the network. Any device can start/stop the chronometer. New devices joining the network automatically join the current chronometer (if already running).

- synclock_masterslave: This is a experimental version where a device acts as a master (press the master connect button to become master) and broadcasts the time to the other devices in the network, which act like slaves. Any device can join at any time and it will be automatically in sync. The timer might be more flacky in this version. This version borrows some code from the nice SyncJams library (https://github.com/chr15m/SyncJams).



Usage and requirements: 

- computer: 
It needs Pure Data and Pddroidparty http://www.droidparty.net/ 
The Synclock version also needs SyncJams https://github.com/chr15m/SyncJams
1. Just open droidparty_main.pd and press the orange button.

- android: 
1. Install the PdDroidparty apk (http://www.droidparty.net) 
4. Send a synclock.dpz file to the any device via email, whatsapp ... 
5. Try to open it. PdDroidParty will launch and run the patch.
6. Press the start button in any of the devices to start the chronometer.
6. From now on just run PdDroidParty and it will offer you to open Synclock



issues:
sometimes it takes a while for all the devices to get to know each other
