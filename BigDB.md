# Everybody Edits Messages Protocol for BigDB
This repository contains documentation on the PlayerIO based [Everybody Edits](http://everybodyedits.com) API.        


## Table of contents
- [BigDB Databases](#BigDB-Databases)
  - [Config](#config)
  - [Usernames](#usernames)
  - [Worlds](#worlds)

### <a id="BigDB-Database">BigDB Databases</a>
A list of current EE BigDB databases

| Name        | Description
| ---         | -----------
| `Config`    | To read server version or admins.
| `Usernames` | Player's usernames.
| `Worlds`    | Player's saved worlds and all their information.  

### <a id="config"> client.BigDB.Load("config","config");
| Text          | Type        | Description
| ---           | ----------- |  -----------            |
| `version`     |  `Integer` | The server version       |
| `betaversion` |  `Integer` | The beta server version  |
| `nextversion` |  `Integer` | The next server version  |
| `scheduled`   |  `DateTime` | No idea.                |
  
### <a id="usernames"> client.BigDB.Load("Usernames","doh");
| Text          | Type          | Description
| ---           | -----------   |  -----------             |
| `owner`       |  `String`     | The players UserID       |
  
### <a id="worlds"> client.BigDB.Load("Worlds","PW01");
| Text            | Type          | Description                                   
| ---             | -----------   |  -----------                                  |
| `width`         |  `Integer`    | The width of the world.                       |
| `height`        |  `Integer`    | The height of the world.                      |
| `type`          |  `Integer`    | If width and height doesn't exist. Use type.  |
| `name`          |  `String`     | The name of the world.                        |
| `plays`         |  `Integer`    | How many plays in the world.                  |
| `owner`         |  `String`     | The UserID of the owner in the world.         |
| `visible`       |  `Boolean`    | The world is visible in lobby.                |
| `Likes`         |  `Integer`    | How many likes the world have.                |
| `Favorites`     |  `Integer`    | How many favorites the world have.            |
| `IsFeatured`    |  `Boolean`    | If the world is in the feature list.          |
| `allowpotions`  |  `Boolean`    | Not used.                                     |
| `enablePotions` |  `Boolean`    | Not used.                                     |
| `woots`         |  `Integer`    | Not used.                                     |
| `totalwoots`    |  `Integer`    | Not used.                                     |
| `coinbanned`    |  `Boolean`    | Not used.                                     |
| `wootbanned`    |  `Boolean`    | Not used.                                     |

