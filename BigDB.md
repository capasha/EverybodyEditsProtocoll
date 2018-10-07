# Everybody Edits Messages Protocol for BigDB
This repository contains documentation on the PlayerIO based [Everybody Edits](http://everybodyedits.com) API.        


## Table of contents
- [BigDB Databases](#BigDB-Databases)
  - [Config](#config)
  - [loadMyPlayerObject](#loadMyPlayerObject)
  - [Usernames](#usernames)
  - [Worlds](#worlds)

### <a id="BigDB-Database">BigDB Databases</a>
A list of current EE BigDB databases

| Name                  | Description
| ---                   | -----------
| `Config`              | To read server version or admins.
| `loadMyPlayerObject`  | Your information.
| `Usernames`           | Player's usernames.
| `Worlds`              | Player's saved worlds and all their information.  

### <a id="config"> client.BigDB.Load("config","config");
| Text          | Type        | Description
| ---           | ----------- |  -----------            |
| `version`     |  `Integer` | The server version       |
| `betaversion` |  `Integer` | The beta server version  |
| `nextversion` |  `Integer` | The next server version  |
| `scheduled`   |  `DateTime` | No idea.                |
  
### <a id="loadMyPlayerObject"> client.BigDB.loadMyPlayerObject();
| Text            | Type          | Description
| ---             | -----------   |  -----------     |
| `Coming Soon`   | `Coming Soon` | Coming Soon      |

### <a id="configstaff"> client.BigDB.Load("config","staff");
| Text          | Type        | Description
| ---           | ----------- |  -----------  
| `Name`        |  `String`   | The role the user have. |
  
### <a id="configpatron"> client.BigDB.Load("config","patrons");
| Text          | Type        | Description
| ---           | ----------- |  -----------  
| `Name`        |  `Integer`   | The patron role the user have. |
  
### <a id="usernames"> client.BigDB.Load("Usernames","doh");
| Text          | Type          | Description
| ---           | -----------   |  -----------             |
| `owner`       |  `String`     | The players UserID       |
  
### <a id="worlds"> client.BigDB.Load("Worlds","PW01");
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
| `worlddata`     |  `Array`      | The blocks in the saved state.                |
| `allowpotions`  |  `Boolean`    | Not used.                                     |
| `enablePotions` |  `Boolean`    | Not used.                                     |
| `woots`         |  `Integer`    | Not used.                                     |
| `totalwoots`    |  `Integer`    | Not used.                                     |
| `coinbanned`    |  `Boolean`    | Not used.                                     |
| `wootbanned`    |  `Boolean`    | Not used.                                     |


### Worlddata
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
