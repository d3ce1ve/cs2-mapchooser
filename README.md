# Map Chooser

---
## Description
This plugin handles basic map voting features like nominate, rtv, extend and end of map voting. It currently only supports
map votes based on `mp_timelimit` but in the future `mp_maxrounds` is planned to be supported to.

---
## API Version
This plugin requires at least API version `198`

---
## Usage
| Command      | Parameter   | Description                                                                                 | Permissions     |
|--------------|-------------|---------------------------------------------------------------------------------------------|-----------------|
| css_nominate |  | Allows you to nominate a cmap to the next map vote list.                                    |
| css_rtv      | | Attemps to start a new map vote when the total number of RTVers passes a certain threshold. | |
| css_unrtv    | | Removes you from the list of people who are trying to rtv.                                  | |

---
## Installation

* Navigate to [releases](https://github.com/justinnobledev/cs2-mapchooser/releases) and download the latest stable
* Extract the zip file to `game/csgo` and it will install to the correct paths
* Edit the `maps.txt` inside of the plugin folder.
  * For workshop maps prepend `ws:` to the name(ex `ws:surf_beginner`)

---
## Future Plans
- [ ] Force map vote admin command
- [ ] Time left command
- [ ] Implement max round for starting map vote

---
## Changelog
```
1.3
Added ua language @panikajo
Added zh_cn language @1370533448
Detecting when someone types rtv in chat
Fixed bots/hltv being detected as a player
Improved vote handling
Auto-swithc on rtv if a map has already been voted for
1.2.6
Added Polish translation - @Letaryat
Added Spanish translation - @criskkky
Mpa votes will now count down on hot reload
Fixed RTV number being wrong due to cs2 bug
Fixed some config values not being read in properly
Fixed infinite RTV after RTV starts
Fixed mapchooser.prefix not ending with {default} and coloring the wrong things
1.2.5
Added new translation for when someone rtv and for when it becomes enabled
Made the time limit enforced an optional config value
Made the time limit forcer end round time based on mp_round_restart_delay
1.2.4
Fixed map not switching
1.2.3
Added an AllowRtv option in the config to turn on and off rtv
1.2.2
Fixed finding mp_match_restart_delay - criskkky
1.2.1
Fixed Config loading
1.2
Fixed event hooking so the map should end at the correct time.
Use TerminateRound method to end the round instead of killing everyone.
1.0
Initital plugin release
```
