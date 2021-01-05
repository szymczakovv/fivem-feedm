<img width="150" height="150" align="left" style="float: left; margin: 0 10px 0 0;" alt="Szymczakovv" src="https://i.imgur.com/42AnCgD.jpg">  

# Standalone FeedM Notification System
[![Paypal Doante](https://img.shields.io/badge/paypal-donate-blue.svg)](https://www.paypal.me/oplatyprimerp)
[![Discord](https://discordapp.com/api/guilds/252317073814978561/embed.png)](https://discord.gg/wrSqK6k)

<p></p>
<p></p>
Standalone FeedM Notification System;
<p></p>
<p></p>
Original: https://github.com/Mobius1/FeedM 
<p></p>
<p></p>
Edited by: https://github.com/elfeedoo & https://github.com/szymczakovv
<p></p>
<p></p>

Changes:
```
FeedM Notification system reworked;

[+] Added custom imgaes e.g your server logo
[+] Added Radar mode = If player is in any vehicle then notify setted positon above Map else notify position setted to under Map
[+] Easy to add new notifications ~ check below.
```
If u are using ESX framework u can easyly add notify;
```
ESX.ShowNotification = function(msg)
	SetNotificationTextEntry('STRING')
	AddTextComponentString(msg)
	DrawNotification(0,1)
end

ESX.ShowAdvancedNotification = function(sender, subject, msg, textureDict, iconType, flash, saveToBrief, hudColorIndex)
	if saveToBrief == nil then saveToBrief = true end
	AddTextEntry('esxAdvancedNotification', msg)
	BeginTextCommandThefeedPost('esxAdvancedNotification')
	if hudColorIndex then ThefeedNextPostBackgroundColor(hudColorIndex) end
	EndTextCommandThefeedPostMessagetext(textureDict, textureDict, false, iconType, sender, subject)
	EndTextCommandThefeedPostTicker(flash or false, saveToBrief)
end

-------------------------------------------
CHANGE TO THIS:
-------------------------------------------

ESX.ShowNotification = function(msg)
    TriggerEvent("FeedM:showNotification", msg)
end

ESX.ShowAdvancedNotification = function(title, subject, msg, icon, color)
    TriggerEvent("FeedM:showAdvancedNotification", title, subject, msg, icon, 5000, ((color and tonumber(color)) and 'primary' or color))
end

```


EXAMPLE SERVER.CFG:
```
ensure mapmanager
ensure chat
ensure spawnmanager
ensure sessionmanager
ensure basic-gamemode
ensure hardcap
ensure rconlog
ensure FeedM
```
If u have questions please write to me on my discord server, not DM.

<p></p>
https://szymczakovv.pl/
<p></p>
https://twitch.tv/szymczakovv
<p></p>
https://instagram.com/szymczakovv/
<p></p>
https://steamcommunity.com/id/szymczakovv

<p></p>
https://discord.gg/wrSqK6k
