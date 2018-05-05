# eLbot's CS:GO Config

This is my personal CS:GO autoexec.cfg which I tweak periodically depending on how focused I am on CS:GO at the time.

Currently I am FOCUSED - monthly changes likely; in lieu of real changelogs, the raw revision changes can be found [here]

The earliest versions of this config will include some odd scripts from Gamebanana purely out of experimentation and to understand what other players might have at their fingertips in fully legal MM servers.

[CEVO/ESEA, Faceit or other leagues or ladders will have their own rules surrounding what is acceptable for a cfg in their games.  It is 100% your responsibility to ensure you are following their rules!!!]

Put "autoexec.cfg" in `...\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg` or selectively pick the parts that you want from it and add to your own manually.

It is important to ensure the config.cfg file also present in this directory isn't set to Read-Only.  

If syncing across steam is enabled (enabling your cfg to travel between machines) the ...Steam\userdata\<Steam3 ID>\730\local\cfg location also houses a config.cfg (which should also not be set to Read-Only) and this is where pushes to the config from autoexec.cfg are currently stored, not the one in ...\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg . If you don't want it to sync on Steam, you can add this to launch options -autoconfig +cl_cloud_settings 0 and then the one in ...\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg will again take precedence.

Autoexec.cfg is automatically run if it is present in this folder without the need of a launch flag.  The launch order is 1)Config.cfg , 2)Autoexec.cfg.  

### Launch Options

These are my current launch options for a 144hz monitor (ASUS ROG PG279)

	-novid -nojoy -freq 144 -refresh 144 -tickrate 128 +cl_forcepreload 1
	
+ -novid: Starting the game with this launch option will remove the Valve intro that normally plays at the beginning.
+ -nojoy: Removes joystick support and increases fps in some cases by reducing memory footprint
+ -freq:
+ -tickrate:
+ +cl_forcepreload:

Enter launch options at `Steam > Library > Counter-Strike: Global Offensive (right-click) > Properties > Set Launch Options...`

### Other Settings
+ 2560x1400, purely preference

### Relevant Hardware
Simply a list of my hardware, will explain logic behind certain settings.
