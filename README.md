# Net64+ Server Startup Scripts (1.0.0)
Startup scripts for the net64+ game server - uses the "screen" command to manage session. This also restarts the net64+ server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/net64PlusStartup) - [Official Forum](https://gameplayer.club/index.php/ourforum/9)

---
These start up the net64+ server at boot time with a "screen" process.

1. Copy **net64plus** into **/etc/init.d** - make sure it is executable
2. Copy **startnet64plus** into **/root/net64plus-server** - make sure it is executable
4. Run "**systemctl enable net64plus**" (only needed once, will stick)
5. Run "**systemctl start net64plus**" - starts net64+ without restarting the server

When you want to view the net64+ console, just enter "**screen -r**" in your shell.

To disconnect from the net64+ console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/net64plus-server/nostart**". To reenable it type "**rm /root/net64plus-server/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
