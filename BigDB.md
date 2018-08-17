# Everybody Edits Messages Protocol for BigDB
This repository contains documentation on the PlayerIO based [Everybody Edits](http://everybodyedits.com) API.        


## Table of contents
- [BigDB Databases](#BigDB-Databases)
  - [Config](#config)
  - [Worlds](#worlds)

### <a id="BigDB-Database">BigDB Databases</a>
A list of current EE BigDB databases

| Name      | Description
| --- | -----------
| `Config` | To read server version or admins.
| `Usernames` | Player's usernames.
| `Worlds` | Player's saved worlds and all their information.  

### client.BigDB.Load("config","config");
| Text      | Type | Description
| --- | ----------- |  ----------- |
| `version` |  `Integer` | The server version |
| `betaversion` |  `Integer` | The beta server version |
| `nextversion` |  `Integer` | The next server version |
| `scheduled` |  `DateTime` | No idea. |

