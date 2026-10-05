# ServerKit-CSGO
This Git provides configs and plugins that are missing from the standard CSGO server. They are installed manually on top of an existing server.

## Installation
1. Install [Metamod](https://www.sourcemm.net/) and [Sourcemod](https://www.sourcemod.net/) on your CSGO server.
2. Download this repository.
3. Copy `addons`, `cfg` and `botprofile.db` into the `csgo` folder of your server and overwrite existing files.
4. Add your admins to `addons/sourcemod/configs/admins_simple.ini`.
5. Restart the server.

## Overview

The core of this Git is the Admin Menu Custom Config, as well as the gamemode_server.cfg files. Thanks to Sourcemod, complete configurations and customizable parameters can be loaded into this menu, making it easy for players with rights to start the mode with their preferences without needing knowledge of the CSGO server's syntax. To make full use of the menu, you should add the [Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=2919873317) Maps to the server. Without it, certain maps cannot be loaded.

Additionally, the package contains some useful plugins and configurations.

## Included Plugins/Extentions
| Name | Description | Version |
|----------|----------|----------|
| [Dhooks 2](https://github.com/peace-maker/DHooks2) | A SourceMod extension to hook any game function from within a SourcePawn plugin. This fork adds support to dynamically detour any functions instead of only virtual functions. | 2.2.0 |
| [SteamWorks](https://github.com/KyleSanderson/SteamWorks) | Exposing SteamWorks functions to SourcePawn. | 1.2.3c |
| [Plugin Enable/Disable](https://forums.alliedmods.net/showthread.php?p=1682844) | Move plugins to and from the disabled folder by command. | 1.0.1 |
| [Time Traveler](https://forums.alliedmods.net/showthread.php?t=134288&page=3) | Ever wanted to run a command in the future? In 10 minutes? In a hour? Now you can! Just enter the timer and the command using sm_futex and this plugin will tunnel into the future and execute your command! | 07-28-2016 YoNer |
| [Bypass Password](https://forums.alliedmods.net/showthread.php?p=2738005) | As you know, in CS:GO game, you can not set sv_password on server if there are players in game. Need to be empty server. This plugin block that check, and allow you set sv_password when ever you like. | 03-02-2023 |
| [Random Password Generation](https://forums.alliedmods.net/showthread.php?t=139990&page=2) | This is a simple plugin that generates a random password. | 06-15-2015 glub |
| [Get5](https://github.com/splewis/get5) | Get5 is a standalone SourceMod plugin for CS:GO servers for running matches. | 0.15.0 |
| [Multi 1v1](https://github.com/splewis/csgo-multi-1v1) | The multi1v1 plugin sets up any number of players in 1v1-situations on specially made maps and they fight in a ladder-type system each round. The winners move up an arena, and the losers go down an arena. Players choose between specific round types (for example: "rifle", "pistol", "awp"), and the plugin automatically spawns and gives players the appropriate weapons each round start. | 1.1.10 |
| [Practice Mode](https://github.com/splewis/csgo-practice-mode) | Practice Mode is a sourcemod plugin for helping players/teams run practices. Check out the features and command list below for a better understanding of all the tools practicemode provides. | 1.3.4 |

These plugins improve or enable different game modes. If you need help using them, you can refer to the plugin's website for more information or visit the [Wiki](https://github.com/Marschux/ServerKit-CSGO/wiki), where all important information is compiled quickly.

## Included Modes
| **Fun Mode** | **Based On** | **Description** |
|----------|----------|----------|
| Casual | [Valve](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) | Used as [Normal](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) mode: Like Competitive but with fewer rounds, shorter freezetime per round, no friendly fire, no team collision, free armor and free defuse kit/cutters. Used as [Trigger Discipline](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes#trigger_Discipline) mode: Gunshots that a player does not hit an enemy with damage himself down to a minimum of 1 HP. |
| Arms Race | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Arms_Race) | The game is one perpetual round where killed players respawn at the default spawns. A weapon progression (a number of guns and their order) is defined where players win by making a specified number of kills with each of these weapons. |
| Crazy Arms Race | [Mashlex](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Arms_Race) | This game mode is a mixture of Arms Race (Speed GunGame) and Free for All Deathmatch. Everyone kills everyone and quickly gets a new weapon. |
| Demolition | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Demolition) | A mixture of Casual with Armsrace. Best of 20 rounds. Each player is given a fixed weapon for each round, depending on his individual progress. Each player can progress one gun per round by making at least one kill. |
| Flying Scoutsman | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes#Flying_Scoutsman) | Only scouts and knives, low gravity, high precision. |
| Solo Danger Zone | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Danger_Zone) | A Battle Royale mode for big maps where players win by being the last man (or team) standing. Maps must be designed for this mode to work as intended. |
| Retake | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes#Retakes) | Each round, 3 Terrorists spawn on a bomb site with a bomb being planted and 4 CTs spawn at fixed locations around it or on the other bomb spot. Each player can choose a loadout card at round start. |
| Guardian | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Guardian) | Two human players must defend a bombsite as CT or hostages as T against rushing bots. Maps must support this mode to work as intended. |
| Aimmaps | [Mashlex](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Deathmatch) | Aimmaps ist ein modus der auf Teamdeathmatch bassiert mit reinen Aimmaps. Zusätzlich kann dies auch noch als "Only Headshot" gestartet werden. |
| Team Deathmatch | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Deathmatch) | Like Armsrace but with free weapon choice and respawns across the map. Kills grant points, depending on the weapon type and if it is currently the bonus weapon. A player wins by scoring the highest after the round's time limit. Only opponents of the other team can be killed. In addition, this mode is also available as a headshot only mode. |
| Free for All | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Deathmatch) | This mode is like the Team Deathmatch mode except that everyone, the opponents as well as your own team, are cleared for shooting. And of course this is also available as a headshot only mode. |
| Practicemode | [Practice Plugin](https://github.com/splewis/csgo-practice-mode) | Practice Mode is a sourcemod plugin for helping players/teams run practices. Check out the features and Practicemode | [command](https://github.com/splewis/csgo-practice-mode) list for a better understanding of all the tools practicemode provides. |
| Arena 1on1 | [Multi 1v1 Plugin](https://github.com/splewis/csgo-multi-1v1) | The multi1v1 plugin sets up any number of players in 1v1-situations on specially made maps and they fight in a ladder-type system each round. The winners move up an arena, and the losers go down an arena. Players choose between specific round types (for example: "rifle", "pistol", "awp"), and the plugin automatically spawns and gives players the appropriate weapons each round start. |
| Aim 1on1 | [Get5 Plugin](https://github.com/splewis/get5) | For 1 vs 1 duels in matchmaking style over 16 rounds. Exclusively on Aimmaps, which are also included in the Prelive Veto. |
| Wingman 2on2 | [Get5 Plugin](https://github.com/splewis/get5) | Like Competitive, but adjusted for 2v2 and for a smaller map or a map section. Best of 16 rounds. Also, each round is shorter. |
| Match 5on5 | [Get5 Plugin](https://github.com/splewis/get5) | The classic game mode, usually made for 5v5. Best of 30 rounds, teams are switched at halftime, friendly fire is on. Round-ending objectives are elimination, bomb explosion, bomb defusal, hostage rescue and timeout. You can choose between three BO1 variants with veto maps. You can choose between Valve Duty Mappool or the maps with other classic Defuse maps. There are also a few hostage maps. And last but not least a No Veto Matchmaking, where the map can be selected manually. | 
| Soft Reset | [Valve](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) | The reset menu item has three options for resetting the server. It is a quick way to reset the serverconfigs without changing the map. |
| Hard Reset | [Valve](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) | The reset menu item has three options for resetting the server. It reload a map and reset the serverconfigs. |
| Full Reset | [Valve](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) | The reset menu item has three options for resetting the server. It restarts the entire server and load the default startoptions setup. |

Some plug-ins have been omitted, such as Deathmatch or Arms Race, which only ask for a little added value. This means that you are not dependent on other plug-ins.

## Custom Server Coammnds
| Command | Description |
|----------|----------|
| Server Password | Generate a random server password and write it in the chat. Or reset the password. When the server is empty, also the server remove the password. | 
| Changelevel | A manual possibility to switch to any map. |
| Mapvote | A possibility to start a poll for the next map. 7 maps can be choose. |
| Restartgame | Restart the game after 3 seconds |
| Bot Quota | Behind this is the command "bot_quota", which changes the number of possible bots. The most modes have _bot_quota_mode fill_ | 
| Bot Add | If the Bots cant join automaticly, then you can add bots. You also can choose the side or kick the bots. | 
| Kick Player | The "Kick Player" function in CSGO allows an administrator to remove a player from the current game. |
| Ban Player | The "Ban Player" function in CSGO allows an administrator to prevent a player from joining the server again. It can be used for rule breaking or disruptive behavior. |
| Reload Admins | When you have added admins via the simple_admin.ini file, you can update the list ingame. |

## Configs 
### Server Config
The server.cfg is the core of the server configs. It contains all the basic settings that are important.
### Gamemodes Configs
The gamemode configs are only links to the existing files. This makes it easy if these files are updated by Valve. Some configs have additional commands that may fix some errors. These are not affected by the Valve updates.
### Gamesettings Configs
These are the config files which can be loaded via the admin menu and which merge the functions of the plugins with the gamemodes. They are also reset again and again through this.
### Mappool INC
These are mappools, very close to the default pools. But they can be easily adapted as desired.
### Adminmenu
The standard "Adminmenu.smx" is edited. The menu items that are normally present have been removed and inserted as required.
### Adminmenu Custom
This file contains the extra gamesetting configurations with the queries for some individual commands. The game mode can be started via the admin menu and adjusted again and again without having to know anything about the source syntax.
### Botprofile
The bug with the rank not being available bothered me. That's why the console no longer shows it. Maybe Valve will fix it one day or HL3 will be released.

## License
The configs and menu files written for this project are licensed under the [GNU General Public License v3.0](LICENSE).

The bundled plugins and extensions (`addons/sourcemod/plugins`, `addons/sourcemod/extensions`) are third-party software under the GPL-3.0, like [SourceMod](https://github.com/alliedmodders/sourcemod) itself. They are redistributed unmodified as compiled binaries; the source code is available at the links in the table above. `botmimic.smx` and `csutils.smx` ship with [Practice Mode](https://github.com/splewis/csgo-practice-mode). `adminmenu.smx` is based on the [SourceMod admin menu](https://github.com/alliedmodders/sourcemod/blob/master/plugins/adminmenu.sp).

`botprofile.db` is a modified game file by Valve / Turtle Rock Studios and is not covered by the GPL. It remains the property of its owners.

This project is not affiliated with or endorsed by Valve. Counter-Strike is a trademark of Valve Corporation.
