# Everybody Edits Messages Protocol for BigDB
This repository contains documentation on the PlayerIO based [Everybody Edits](http://everybodyedits.com) API.        
To use BigDB you need to login to Everybody Edits. Use this code as example: client.BigDB.

## Table of contents
- [BigDB Databases](#BigDB-Databases)
  - [Config](#config)
  - [LoadMyPlayerObject](#LoadMyPlayerObject)
  - [PlayerObjects](#playerobjects) 
  - [Usernames](#usernames)
  - [Worlds](#worlds)


### <a id="BigDB-Database">BigDB Databases</a>
A list of current EE BigDB databases

| Name                  | Description
| ---                   | -----------
| `Config`              | To read server version or admins.
| `LoadMyPlayerObject`  | Your information.
| `PlayerObjects`  		| The user information (Need userid).
| `Usernames`           | Player's usernames.
| `Worlds`              | Player's saved worlds and all their information.   

### <a id="config"> Load("config","config");
| Text          | Type        | Description
| ---           | ----------- |  -----------            |
| `version`     |  `Integer` | The server version       |
| `betaversion` |  `Integer` | The beta server version  |
| `nextversion` |  `Integer` | The next server version  |
| `scheduled`   |  `DateTime` | No idea.                |

### <a id="configstaff"> Load("config","staff");
| Text          | Type        | Description
| ---           | ----------- |  -----------  
| `Name`        |  `String`   | The role the user have. |
  
### <a id="configpatron"> Load("config","patrons");
| Text          | Type        | Description
| ---           | ----------- |  -----------  
| `Name`        |  `Integer`   | The patron role the user have. |
  
### <a id="LoadMyPlayerObject"> LoadMyPlayerObject();    
| Text               | Type          | Description
| ---                | -----------   |  -----------                                      |
| `maxEnergy`        | `Integer`     | Your max Energy.                                  |
| `name`             | `String`      | Your nickname in EE.                              |
| `shopItems`        | `Array`       | Shop Items.                                       |
| `lastcoin`         | `DateTime`    | When you got your last magic coin.                |
| `world00x99`       | `String`      | The worlds you have bought.                       |
| `visible`          | `Boolean`     | If people can see your profile or not.            | 
| `betaonlyroom`     | `String`      | Your beta world.                                  | 
| `smiley`           | `Integer`     | Your current used smiley.                         |
| `myworldnames`     | `Array`       | Your worlds names.                                |
| `room0`            | `String`      | Your first world with beta.                       |
| `timezone`         | `Integer`     | Your timezone.                                    |
| `worldhome`        | `String`      | Your home world.                                  |
| `termsVersion`     | `Integer`     | This is the terms that you have accepted.         |
| `aura`             | `Integer`     | Your current selected aura.                       |
| `auraColor`        | `Integer`     | Your current selected aura color.                 |
| `likes`            | `Array`       | Your list of worlds that you have liked.          |
| `badge`            | `String`      | Your current selected badge.                      |
| `loginStreak`      | `Integer`     | Your current loginstreak.                         |
| `favorites`        | `Array`       | Your list of worlds that you have favorited.      |
| `gold_expire`      | `DateTime`    | When your golden member will end.                 |
| `gold_join`        | `DateTime`    | Your first time you joined as golden member.      |
| `smileyGoldBorder` | `Boolean`     | If you have activated golden border or not.       |
| `shopDate`         | `DateTime`    | Last time you bought something through the shop.  |
| `energyDelay`      | `Integer`     | This is the delay for how fast you get energy.    |

### <a id="PlayerObjects"> Load("PlayerObjects","simpleguest");  
| Text               | Type          | Description
| ---                | -----------   |  -----------                                    		  			|
| `maxEnergy`        | `Integer`     | The User max Energy.                            		 			|
| `name`             | `String`      | The User nickname in EE.                              			|
| `shopItems`        | `Array`       | Shop Items.                                     		  			|
| `lastcoin`         | `DateTime`    | When the User got the last magic coin.                			|
| `world00x99`       | `String`      | The worlds The User have bought.                       			|
| `visible`          | `Boolean`     | If people can see the user profile or not.         	  			| 
| `betaonlyroom`     | `String`      | The User beta world.                                  			| 
| `smiley`           | `Integer`     | The User current used smiley.                         			|
| `myworldnames`     | `Array`       | The User worlds names.                                			|
| `room0`            | `String`      | The User first world with beta.                       			|
| `timezone`         | `Integer`     | The User timezone.                                    			|
| `worldhome`        | `String`      | The User home world.                                 			|
| `termsVersion`     | `Integer`     | This is the terms that the user have accepted.         			|
| `aura`             | `Integer`     | The User current selected aura.                       			|
| `auraColor`        | `Integer`     | The User current selected aura color.                 			|
| `likes`            | `Array`       | The User list of worlds that you have liked.          			|
| `badge`            | `String`      | The User current selected badge.                      			|
| `loginStreak`      | `Integer`     | The User current loginstreak.                         			|
| `favorites`        | `Array`       | The User list of worlds that you have favorited.      			|
| `gold_expire`      | `DateTime`    | The User golden member will end.                			 		|
| `gold_join`        | `DateTime`    | The User first time that the User joined as golden member.  		|
| `smileyGoldBorder` | `Boolean`     | If the User have activated golden border or not.      			|
| `shopDate`         | `DateTime`    | Last time the User bought something through the shop.  			|
| `energyDelay`      | `Integer`     | This is the delay for how fast the User get energy.    			|
  
### <a id="usernames"> Load("Usernames","doh");
| Text          | Type          | Description
| ---           | -----------   |  -----------                |
| `owner`       |  `String`     | The players UserID or none  |
| `oldowner`    |  `String`     | The players old UserID      |
  
### <a id="worlds"> Load("Worlds","PW01");
| Text            | Type          | Description                                   
| ---             | -----------   |  -----------                                  |
| `width`         |  `Integer`    | The width of the world.                       |
| `height`        |  `Integer`    | The height of the world.                      |
| `type`          |  `Integer`    | If width and height doesn't exist. [Use type](#worlds-type).  |
| `name`          |  `String`     | The name of the world.                        |
| `plays`         |  `Integer`    | How many plays in the world.                  |
| `owner`         |  `String`     | The UserID of the owner in the world.         |
| `visible`       |  `Boolean`    | The world is visible in lobby.                |
| `Likes`         |  `Integer`    | How many likes the world have.                |
| `Favorites`     |  `Integer`    | How many favorites the world have.            |
| `IsFeatured`    |  `Boolean`    | If the world is in the feature list.          |
| `worlddata`     |  `Array`      | The blocks in the saved state. [Contains](#WorldData)                |
| `allowpotions`  |  `Boolean`    | Not used.                                     |
| `enablePotions` |  `Boolean`    | Not used.                                     |
| `woots`         |  `Integer`    | Not used.                                     |
| `totalwoots`    |  `Integer`    | Not used.                                     |
| `coinbanned`    |  `Boolean`    | Not used.                                     |
| `wootbanned`    |  `Boolean`    | Not used.                                     |


### <a id="WorldData"> Worlddata
| Id        | Type         | Description
| -----     | ------------ | ------------                                           |
| `type`      | `UInt`            | The id of the block.                            | 
| `layer`     | `Integer`         | The layer, bg or fg.                            |
| `goal`      | `Integer`         | Coin Door/Gate.                                 |
| `signtype`  | `Integer`         | The sign type.                                  |
| `rotation`  | `Integer`         | Rotation of the block.                          |
| `id`        | `Integer`         | Id for sound or portal.                         |
| `name`      | `String`          | Name of the NPC.                                |
| `mes1`      | `String`          | Message 1 of the NPC.                           |
| `mes2`      | `String`          | Message 2 of the NPC.                           |
| `mes3`      | `String`          | Message 3 of the NPC.                           |
| `target`    | `Integer & String`| Both string or integer. worldportal or Portal.  |
| `text`      | `String`          | Text for sign, worldportal or admintext.        |
| `text_color`| `String`          | Color for Admin text.                           |
| `x`         | `ByteArray`       | X locations in a ByteArray. (Needs Bitshifting) |
| `y`         | `ByteArray`       | Y locations in a ByteArray. (Needs Bitshifting) |
| `x1`        | `ByteArray`       | X1 locations in a ByteArray. (Needs Bitshifting) |
| `y1`        | `ByteArray`       | Y1 locations in a ByteArray. (Needs Bitshifting) |

<a href="https://pastebin.com/WStXbMux">Example how to read from Worldata</a>

# Data
### <a id="worlds-type"> Worlds Type
| ID    | World Size
| ----- | ------------
| `1`     | 50x50      |
| `2`     | 100x100    |
| `3`     | 200x200    |
| `4`     | 400x50     |
| `5`     | 400x200    |
| `6`     | 100x400    |
| `7`     | 636x50     |
| `8`     | 110x110    |
| `11`    | 300x300    |
| `12`    | 200x150    |
| `13`    | 150x150    |
