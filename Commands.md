This list is outdated. Will be updated in the future.
# Table of Contents
- [Owner only commands](#commands-owner)
  - [/bgcolor](#command-bgcolor)
  - [/clear](#command-clear)
  - [/cleareffects /ce](#command-cleareffects)
  - [/forcefly](#command-forcefly)
  - [/forgive](#command-forgive)
  - [/givecrown](#command-givecrown)
  - [/giveedit /gedit /ge](#command-giveedit)
  - [/giveeffect /geffect](#command-giveeffect)
  - [/givegod](#command-givegod)
  - [/hidelobby](#command-hidelobby)
  - [/kick](#command-kick)
  - [/kill](#command-kill)
  - [/killall](#command-killall)
  - [/listportals](#command-listportals)
  - [/loadlevel](#command-loadlevel)
  - [/removecrown](#command-removecrown)
  - [/removeedit /redit /re](#command-removeedit)
  - [/removeeffect](#command-removeeffect)
  - [/removegod](#command-removegod)
  - [/reset](#command-reset)
  - [/resetall](#command-resetall)
  - [/respawnall](#command-respawnall)
  - [/setteam](#command-setteam)
  - [/teleport /tele /tp](#command-teleport)
  - [/visible](#command-visible)
- [Commands for everyone](#commands-everyone)
  - [/clearchat](#command-clearchat)
  - [/getpos](#command-getpos)
  - [/help](#command-help)
  - [/inspect](#command-inspect)
  - [/mute](#command-mute)
  - [/pm](#command-pm)
  - [/reportabuse /report /rep](#command-reportabuse)
  - [/roomid](#command-roomid)
  - [/spectate /spec](#command-spectate)
  - [/unumte](#command-unmute)

# <a id="commands-owner">Owner only commands</a>

### <a id="command-bgcolor">/bgcolor /bc</a>
Change the world's background color.

#### `/bgcolor #{6 digit color hex}`
Set background to color corresponding to the specified hexadecimal value.
- `{6 digit color hex}` - The hexadecimal value of color to use.

#### `/bgcolor none`
Remove background color. 

___
### <a id="command-clear">/clear</a>
Clear the world.

*No arguments*

___
### <a id="command-cleareffects">/cleareffects /ce</a>
Remove all effects from player.

#### `/cleareffects {username}`
Remove all effects from player with the specified username.

- `{username}` - The username of player from which to remove effects.

___
### <a id="command-forcefly">/forcefly</a>
Activate or deactivate flying mode of player.

#### `/forcefly {username} true`
Activate flying mode of player with the specified username.
NOTE: If player doesn't have flying privilegess he won't be able to leave flying mode.

#### `/forcefly {username} false`
Deactivate flying mode of player with the specified username.

- `{username}` - Username of the player for who to activate or deactivate flying mode.

___
### <a id="command-forgive">/forgive</a>
Forgive a player that you kicked.

#### `/forgive {username}`
Makes so the player can join directly after a kick.

- `{username}` - Username of the player for which to forgive.

___
### <a id="command-givecrown">/givecrown</a>
Give crown to a player.

#### `/givecrown {username}`
Give crown to a player with the specified username.

- `{username}` - Username of the player for which to give crown.

___
### <a id="command-giveedit">/giveedit /gedit /ge</a>
Give edit right to a player.

#### `/giveedit {username}`
Give edit rights to a player with the specified username.

- `{username}` - Username of the player for which to give edit rights.

___
### <a id="command-giveeffect">/giveeffect /geffect</a>
Give effect to a player.

#### `/giveeffect {username} {effect}`
Give specified effect to a player with specified username.

- `{username}` - Username of the player for which to give effect.
- `{effect}` - The effect to give. For available options see: [Effects](#effects)

___
### <a id="command-givegod">/givegod</a>
Give flying rights to a player.

#### `/givegod {username}`
Give flying rights to a player with the specified username.
NOTE: Player will be able to manually toggle flying mode after using this command.

- `{username}` - Username of player for which to give flying rights.

___
### <a id="command-hidelobby">/hidelobby</a>
Set world as visible or hidden from the lobby.

#### `/hidelobby true`
Make the world invisible in the lobby.

### `/hidelobby false`
Make the world visible in the lobby.

___
### <a id="command-kick">/kick</a>
Kick a player from the world.

#### `/kick {username}`
Kick a player with the specified username.

#### `/kick {username} {reason}`
Kick a player with the specified username and display to him the specified message.

- `{username}` - Username of player to kick.
- `{reason}` - Message to display to player after kicking.

___
### <a id="command-kill">/kill</a>
Kill a player.

#### `/kill {username}`
Kill a player with the specified username.

- `{username}` - Username of player to kill.

___
### <a id="command-killall">/killall</a>
Kill all players in the world.

*No arguments*

___
### <a id="command-listportals">/listportals</a>
List positions and source/target id's of all portals placed in the world.

*No arguments*

___
### <a id="command-loadlevel">/loadlevel</a>
Reset the world to last save.

*No arguments*

___
### <a id="command-removecrown">/removecrown</a>
Remove crown from a player which is currently wearing it.

*No arguments*

___
### <a id="command-removeedit">/removeedit /redit /re</a>
Take away edit rights from a player.

#### `/removeedit {username}`
Take away edit rights from a player with the specified username.

- `{username}` - Username of player from which to remove edit rights.

___
### <a id="command-removeeffect">/removeeffect</a>
Remove effect from a player.

#### `/removeeffect {username} {effect}`
Remove specified effect from a player with the specified username.

- `{username}` - Username of the player from which to remove effect.
- `{effect}` - The effect to remove. For available options see: [Effects](#effects)

___
### <a id="command-removegod">/removegod</a>
Remove flying rights of a player.
NOTE: After using this command player will automatically leave flying mode.

#### `/removegod {username}`
Remove flying rights of a player with the specified username.

- `{username}` - Username of player from which to remove flying rights.

___
### <a id="command-reset">/reset</a>
Reset player by removing their deaths, coins, effects, etc.

#### `/reset`
Reset yourself.

#### `/reset {username}`
Reset player with the specified username.

- `{username}` - Username of the player to reset.

___
### <a id="command-resetall">/resetall</a>
Reset all player located in the world.

*No arguments*

___
### <a id="command-respawnall">/respawnall</a>
Move all players to their last checkpoint.

*No arguments*

___
### <a id="command-setteam">/setteam</a>
Move player to a team.

#### `/setteam {username} {team}`
Move player with the specified username to the specified team.

- `{username}` - Username of player for which to change team.
- `{team}` - Team to which to move player. For available options see: [Teams](#teams)

___
### <a id="command-teleport">/teleport /tele /tp</a>
Teleport player to different position.

#### `/teleport {username}`
Teleport player with the specified username to yourself.

#### `/teleport {username} {target}`
Teleport player with the specified username to player with target username.

#### `/teleport {username} {x} {y}`
Teleport player with the specified username to the specified coordinates.

- `{username}` - Username of player to teleport.
- `{target}` - Username of player to which to teleport.
- `{x}` - x coordinate of target position.
- `{y}` - y coordinate of target position.

___
### <a id="command-visible">/visible</a>
Set the world as (in)accessible to others.

#### `/visible true`
Make the world accessible by other players.

#### `/visible false`
Prevent other players from joining the world.

___

# <a id="commands-everyone">Commands for everyone</a>

### <a id="command-clearchat">/clearchat</a>
Clear the chat log.

*No arguments*

___
### <a id="command-getpos">/getpos</a>
Get position of a player.

#### `/getpos`
Get your own position.

#### `/getpos {username}`
Get position of a player with the specified username.

- `{username}` - Username of player of which to get position.

___
### <a id="command-help">/help</a>
Display list of available commands.

*No arguments*

___
### <a id="command-inspect">/inspect</a>
Toggle the inspect tool.

*No arguments*

___
### <a id="command-mute">/mute</a>
Mute a player.

#### `/mute {username}`
Mute a player with the specified username.

- `{username}` - Username of player to mute.

___
### <a id="command-pm">/pm</a>
Send a private message to other player.

#### `/pm {username} {message}`
Send the specified message to a player with the specified username.

- `{username}` - Username of player to which to send private message.
- `{message}` - The private message to send.

___
### <a id="command-reportabuse">/reportabuse /report /rep</a>
Report a player for breaking the rules.

#### `/reportabuse {username} {reason}`
Report a player with the spcified username for the spcified reason.

- `{username}` - Username of the player to report.
- `{reason}` - Reason why the player gets reported.

___
### <a id="command-roomid">/roomid</a>
Display id of the world.

*No arguments*

___
### <a id="command-spectate">/spectate /spec</a>
Start or stop spectating a player.

#### `/spectate`
Stop spectating.

#### `/spectate {username}`
Start spectating player with the specified username.

#### `/spectate {myusername}`
Stop spectating.

- `{username}` - Username of player to spectate.
- `{myusername}` - Your own username.

___
### <a id="command-unmute">/unmute</a>
Unmute a player.

#### `/unmute {username}`
Unmute player with the specified username.

- `{username}` - Username of player to unmute.
