# How to connect to Lobby
[Connect to Lobby (Pastebin)](https://pastebin.com/A8YGNyum)

## Send messages
### Get Information
| Command               | Parameters | Description
| ------                | ---------- | -----------                                            |
| `getShop`             | None       | Get the Shop Data                                      |
| `getFriends`          | None       | Get data from friends in the friendlist.               |
| `getInvitesToMe`      | None       | Get friend invites that someone have sent.             |
| `getPending`          | None       | Get friend pending invites.                            |
| `getBlockedUsers`     | None       | Get friends invites that you have blocked.             |
| `getProfileObject`    | `Nickname` | Get the users information, such as world and smileyid. |
| `getCrews`            | `Nickname` | Get in which crews the user is in.                     |
| `getCrew`             | `CrewName` | Get information about a crew.                          |
| `isSubscribedToCrew`  | `CrewID`   | Check if you are subscribed to the crew.               |
| `getBlockStatus`      | None       | Checks if blocking friend request is on or off         |
| `getProfile`          | None       | Checks if your profile is private or not               |

### Send Information
| Command               | Parameters            | Description
| ------                | ----------            | -----------                                            |
| `createCrew`          | `CrewName`            | Create a new crew.                                     |
| `changeSmiley`        | `SmileyID`            | Change your smiley.                                    |
| `changeAura`          | `AuraID`,`AuraColor`  | Change your aura and aura color                        |
