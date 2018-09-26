# eLbot's CS:GO Config

This is my personal CS:GO autoexec.cfg which I tweak periodically depending on how focused I am on CS:GO at the time.  It has not yet seen a major overhaul since the panorama update broke some minor bits of functionality (dmg prints etc).

Currently I am not really attached to the game.  Last edit: 24/09/2018.

The earliest versions of this config will include some odd scripts from Gamebanana purely out of experimentation and to understand what other players might have at their fingertips in fully legal MM servers.

### [CEVO/ ESEA, Faceit or other leagues/ ladders will have their own rules surrounding what is acceptable in a cfg for their games.  It is 100% your responsibility to ensure you are following their rules!!!]

Put "autoexec.cfg" in `...\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg` or selectively pick the parts that you want from it and add to your own manually.

It is important to ensure the config.cfg file also present in this directory isn't set to Read-Only.  

If syncing across steam is enabled (enabling your cfg to travel between machines) the

`...Steam\userdata\<STEAM_ID>\730\local\cfg` location also houses a `config.cfg` (which should also not be set to Read-Only) and this is where pushes to the config from `autoexec.cfg` via `host_writeconfig` are currently stored, not the one in 

`...\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg` as other documentation suggests. If you don't want it to sync on Steam, you can add this to launch options `-autoconfig +cl_cloud_settings 0` and then the one in 

`...\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg` will again take precedence. 

## Current Scripts / Useful commands

+ DMG Display: Toggles On/Off the Printing of end of round damage stats directly above radar without the need to check console, also highlights those damage entries in console whilst toggled ON.
+ Team Equipment: Toggles On/Off the Display of team equipment data, allowing some position information to be taken on teammates through walls and full knowledge of their equipment loadout.  There is the option to call this script on reload or scoreboard if wanted.
+ Jumpthrow: A Commonly used grenade throw that is tricky to perform reliably without such a script.
+ Print Logic: The commands "xhair" and "viewmod" etc are created to print and highlight associated config settings. (Hoping to expand to most of the first 10 steps eventually).
+ cl_teamid_overhead_always "1":  Place Arrow above team-mates (Even through walls... volvo!?!)

## Launch Options

Autoexec.cfg is automatically run if it is present in this folder without the need of a launch flag.  
The launch order is 1) Config.cfg THEN 2) Autoexec.cfg. 

These are my current launch options:

	-novid -nojoy -tickrate 128 +cl_forcepreload 1
	
+ -novid: Starting the game with this launch option will remove the Valve intro that normally plays at the beginning.
+ -nojoy: Removes joystick support and increases fps in some cases by reducing memory footprint
+ -tickrate 128: Makes any local server run at 128tk (useful vs bot games if you've long left MM in the dirt)
+ +cl_forcepreload 1: Preloads map and sound assets. (supposedly... still see about 40% of it loading during first event rather than precalled.)

Enter launch options at `Steam > Library > Counter-Strike: Global Offensive (right-click) > Properties > Set Launch Options...`

## Other Settings
+ 2560x1440, purely preference
<To Do> - Windows settings / regfile changes if any are still relevant.

## Relevant Hardware
Simply a list of my hardware, will explain some of the logic behind certain settings.

+ Mouse: Zowie EC2-A
+ Mouse Surface: Steel-Series Dex
+ Keyboard: Steel-Series 7G (Blacks)
+ Headset: Sennheiser Game ONE - Open headset
+ Soundcard: Sennheiser 3DG4ME1
+ Monitor: Asus ROG PG279 set to 144hz
+ GPU: 1080Ti
+ Net connection: UK - Virgin Media Vivid 200; giving 230dn/12up from Ookla and averaging a 20-30ms connection to closest node.

## Things discovered as a result of this process.

+ The Range Casting of connections and what that means for pings now.
+ That you can view your team's equipment at all never-lone through walls!
+ That you can print your damage stats directly into window above radar!
+ That it's possible to create moderate print logic for some groups of settings.

## To-Do

+ Make custom radio menus for mute settings

## Acknowledgements

+ Xhair and Viewmod settings print logic first adapated from Iwan0ffwOw~'s scripts on Gamebanana.
