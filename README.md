# synclock a0.3

2019/05/08

by ixi-audio.net and supported by the University of the Basque Country http://www.ehu.eus


A chronometer that runs in sync in many devices at the same time (android and pcs). Developed in PureData

License GPL

Synclock is an atempt to create a chronometer that runs in sync in many devices at the same time. The devices must be in the same network (firewalls might interfiere). It is programmed in PD.

- It displays the current time with 00:00 format (max 59:59)
- It displays the current bar 
- Countdown 3-2-1-0 with a red flash before starting
- Flashes at BPM

There are two versions:

- synclock: It uses the SyncJams library (https://github.com/chr15m/SyncJams) to syncronise all devices in the local network. The time is shared between all devices in the network. Any device can start/stop the chronometer. New devices joining the network automatically join the current chronometer (if already running).

- synclock_masterslave: This is a experimental version where a device acts as a master (press the master connect button to become master) and broadcasts the time to the other devices in the network, which act like slaves. Any device can join at any time and it will be automatically in sync. The timer might be more flacky in this version. This version borrows some code from the nice SyncJams library (https://github.com/chr15m/SyncJams).



Usage and requirements: 

- computer: 
It needs Pure Data and Pddroidparty http://www.droidparty.net/ 
The Synclock version also needs SyncJams https://github.com/chr15m/SyncJams
1. Just open droidparty_main.pd and press the orange button.

- android + iOS: 
1a. Android: Install the PdDroidparty apk (http://www.droidparty.net) 
1b. iOS: Install PdParty (https://itunes.apple.com/app/id970528308)
4. Send a synclock.pdz file to the device via email, whatsapp ... 
5. Try to open it. PdDroidParty/PdParty should run it or copy it to the phone to later run it
6. To start one of the users must press the start button (orange, top-left) and all clients connected should see the flashing countdown for 4 secs and later get the chronometer in sync.
6. From now on just run PdDroidParty/PdParty and it will offer you to open Synclock.



issues:
sometimes it takes a while for all the devices to get to know each other. no idea why.
