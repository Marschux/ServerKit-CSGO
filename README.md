# ServerKit-CSGO
This repository provides configs and plugins that a standard CS:GO server does not ship with. They are installed manually on top of an existing server.

## Installation
1. Install [Metamod](https://www.sourcemm.net/) and [SourceMod](https://www.sourcemod.net/) on your CS:GO server.
2. Download this repository.
3. Copy `addons`, `cfg`, `match`, `mapcycle.txt` and `maplist.txt` into the `csgo` folder of your server and overwrite existing files.
4. Add your admins to `addons/sourcemod/configs/admins_simple.ini` and set your own `rcon_password` in `cfg/server.cfg` (empty by default, which disables RCON).
5. Restart the server.

## Overview

The core of this repository is the custom admin menu config together with the `gamemode_*_server.cfg` files. The menu loads complete configurations with adjustable parameters, so admins can start a game mode with their own preferences without knowing the CS:GO server syntax. To make full use of the menu, add the [Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=2919873317) map collection to the server. Without it, some maps cannot be loaded.

The package also contains several useful plugins and configurations.

## Included Plugins/Extensions
| Name | Description | Version |
|----------|----------|----------|
| [SteamWorks](https://github.com/KyleSanderson/SteamWorks) | Exposes SteamWorks functions to SourcePawn. | 1.2.3c |
| [Plugin Enable/Disable](https://forums.alliedmods.net/showthread.php?p=1682844) | Moves plugins to and from the disabled folder by command. | 1.0.1 |
| [Time Traveler](https://forums.alliedmods.net/showthread.php?t=134288&page=3) | Runs a command after a delay. Pass a timer and a command to `sm_futex`, and the plugin executes the command once the timer has elapsed. | 07-28-2016 YoNer |
| [Bypass Password](https://forums.alliedmods.net/showthread.php?p=2738005) | CS:GO normally only allows setting `sv_password` while the server is empty. This plugin removes that check, so the password can be set at any time. | 03-02-2023 |
| [Random Password Generation](https://forums.alliedmods.net/showthread.php?t=139990&page=2) | Generates a random server password. | 06-15-2015 glub |
| [Get5](https://github.com/splewis/get5) | A standalone SourceMod plugin for running matches on CS:GO servers. | 0.15.0 |
| [Multi 1v1](https://github.com/splewis/csgo-multi-1v1) | Puts any number of players into 1v1 arenas on specially made maps, in a ladder system: each round the winner moves up an arena and the loser moves down. Players choose a round type (for example "rifle", "pistol" or "awp") and receive the matching weapons at round start. | 1.1.10 |
| [Practice Mode](https://github.com/splewis/csgo-practice-mode) | Helps players and teams run practices. See the feature and command list on the plugin's page for all the tools it provides. | 1.3.4 |

These plugins improve or enable the game modes below. If you need help using one of them, refer to the plugin's page.

## Included Modes
| **Mode** | **Based On** | **Description** |
|----------|----------|----------|
| Casual | [Valve](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) | As [Normal](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) mode: like Competitive, but with fewer rounds, a shorter freeze time, no friendly fire, no team collision, free armor and a free defuse kit. As [Trigger Discipline](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes#trigger_Discipline) mode: shots that miss an enemy damage the shooter, down to a minimum of 1 HP. |
| Arms Race | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Arms_Race) | One perpetual round in which killed players respawn at the default spawns. Players advance through a fixed weapon progression and win by making the required number of kills with each weapon. |
| Crazy Arms Race | [Marschux](https://github.com/Marschux) | A mixture of Arms Race (speed gun game) and Free for All Deathmatch. Everyone fights everyone and gets a new weapon quickly. |
| Demolition | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Demolition) | A mixture of Casual and Arms Race, best of 20 rounds. Each player gets a fixed weapon per round, depending on individual progress, and advances one weapon per round by making at least one kill. |
| Flying Scoutsman | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes#Flying_Scoutsman) | Only scouts and knives, low gravity, high accuracy. |
| Solo Danger Zone | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Danger_Zone) | A battle royale mode for big maps, won by the last player (or team) standing. Maps must be designed for this mode. |
| Retake | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes#Retakes) | Each round, 3 Terrorists spawn on a bomb site with the bomb already planted, and 4 CTs spawn at fixed locations around it or on the other site. Each player chooses a loadout card at round start. |
| Guardian | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Guardian) | Two human players defend a bomb site as CTs, or hostages as Ts, against rushing bots. Maps must support this mode. |
| Aimmaps | [Marschux](https://github.com/Marschux) | A mode based on Team Deathmatch that is played on pure aim maps. Also available as a headshot-only mode. |
| Team Deathmatch | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Deathmatch) | Like Arms Race, but with free weapon choice and respawns across the map. Kills grant points depending on the weapon type and on whether it is the current bonus weapon. The player with the highest score at the end of the time limit wins. Only players of the other team can be killed. Also available as a headshot-only mode. |
| Free for All | [Valve](https://developer.valvesoftware.com/wiki/CS:GO_Game_Modes/Deathmatch) | Like Team Deathmatch, except that everyone can be killed, including your own team. Also available as a headshot-only mode. |
| Practicemode | [Practice Plugin](https://github.com/splewis/csgo-practice-mode) | Helps players and teams run practices. See the feature and [command list](https://github.com/splewis/csgo-practice-mode) for all the tools it provides. |
| Arena 1on1 | [Multi 1v1 Plugin](https://github.com/splewis/csgo-multi-1v1) | Puts any number of players into 1v1 arenas on specially made maps, in a ladder system: each round the winner moves up an arena and the loser moves down. Players choose a round type (for example "rifle", "pistol" or "awp") and receive the matching weapons at round start. |
| Aim 1on1 | [Get5 Plugin](https://github.com/splewis/get5) | 1v1 duels in matchmaking style over 16 rounds. Played only on aim maps, which are picked by veto before the match goes live. |
| Wingman 2on2 | [Get5 Plugin](https://github.com/splewis/get5) | Like Competitive, but adjusted for 2v2 on a smaller map or map section. Best of 16 rounds, with shorter rounds. |
| Match 5on5 | [Get5 Plugin](https://github.com/splewis/get5) | The classic 5v5 mode. Best of 30 rounds, teams switch sides at halftime, friendly fire is on. Rounds end by elimination, bomb explosion, bomb defusal, hostage rescue or timeout. There are three BO1 variants with map veto: Valve's Active Duty map pool, a pool with other classic defuse maps, and a few hostage maps. A variant without veto lets you select the map manually. |
| Soft Reset | [Valve](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) | Resets the server configs without changing the map. The quickest of the three reset options. |
| Hard Reset | [Valve](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) | Reloads the map and resets the server configs. |
| Full Reset | [Valve](https://developer.valvesoftware.com/wiki/Creating_a_Classic_Counter-Strike_Map) | Restarts the entire server and loads the default startup setup. |

Modes such as Deathmatch and Arms Race run without extra plugins, because a plugin would add little value there. This keeps the kit independent of further plugins.

## Custom Server Commands
| Command | Description |
|----------|----------|
| Server Password | Generates a random server password and writes it to the chat, or resets the password. The password is also removed automatically when the server is empty. |
| Changelevel | Switches manually to any map. |
| Mapvote | Starts a vote for the next map. Up to 7 maps can be offered. |
| Restartgame | Restarts the game after 3 seconds. |
| Bot Quota | Sets `bot_quota`, the number of bots on the server. Most modes use `bot_quota_mode fill`. |
| Bot Add | Adds bots manually if they do not join automatically. You can also choose their side or kick them. |
| Kick Player | Removes a player from the current game. |
| Ban Player | Prevents a player from joining the server again, for example after rule breaking or disruptive behavior. |
| Reload Admins | Reloads the admin list in game after you have changed the `admins_simple.ini` file. |

## Configs
### Server Config
The `server.cfg` is the core of the server configs. It contains all the important basic settings.
### Gamemodes Configs
The `gamemode_*_server.cfg` files only execute Valve's existing gamemode configs, so updates from Valve are picked up automatically. Some of them contain additional commands that fix known errors. These additions are not affected by Valve updates.
### Gamesettings Configs
These configs are loaded through the admin menu and combine the plugins with the game modes. Each one first resets plugins and settings, so you can switch between modes at any time.
### Mappool INI
These are map pools that stay close to the default pools. They can easily be adapted as desired.
### Adminmenu
The standard `adminmenu.smx` has been modified: the default menu categories are removed, and the items are added back only where needed.
### Adminmenu Custom
This file contains the game mode entries of the menu, including the prompts for individual parameters. A mode can be started and adjusted through the admin menu without knowing the server syntax.
### Botprofile
The stock `botprofile.db` prints an error for every `Rank = ...` line on server start. The file belongs to Valve and is not included here. To silence the errors, open `csgo/botprofile.db` on your server and comment out the 8 `Rank` lines by putting `//` in front of them.

## License
The configs and menu files written for this project are licensed under the [GNU General Public License v3.0](LICENSE).

The bundled plugins and extensions (`addons/sourcemod/plugins`, `addons/sourcemod/extensions`) are third-party software under the GPL-3.0, like [SourceMod](https://github.com/alliedmodders/sourcemod) itself. They are redistributed unmodified as compiled binaries; the source code is available at the links in the table above. `botmimic.smx` and `csutils.smx` ship with [Practice Mode](https://github.com/splewis/csgo-practice-mode). `adminmenu.smx` is a modified build of the SourceMod 1.11 admin menu without the three default categories; its source is in `addons/sourcemod/scripting`.

This project is not affiliated with or endorsed by Valve. Counter-Strike is a trademark of Valve Corporation.
