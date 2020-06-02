# How to connect to Lobby
[Connect to Lobby (Pastebin)](https://pastebin.com/A8YGNyum)  
[Loop through ss and se settings(Pastebin)](https://pastebin.com/iBGW0TUa)  

## Send messages
### Get Information
| Command               	| Parameters | Description
| ------                	| ---------- | -----------                                            |
| `getShop`             	| None       | Get the Shop Data                                      |
| `getFriends`          	| None       | Get data from friends in the friendlist.               |
| `getInvitesToMe`      	| None       | Get friend invites that someone have sent.             |
| `getPending`          	| None       | Get friend pending invites.                            |
| `getBlockedUsers`     	| None       | Get friends invites that you have blocked.             |
| `getProfileObject`    	| `Nickname` | Get the users information, such as world and smileyid. |
| `getMySimplePlayerObject` | None   	 | Get settings and your playerobject information.        |
| `getCrews`            	| `Nickname` | Get in which crews the user is in.                     |
| `getCrew`             	| `CrewName` | Get information about a crew.                          |
| `isSubscribedToCrew`  	| `CrewID`   | Check if you are subscribed to the crew.               |
| `getMyCrews`         		| None       | Get all your crews you are in.                         |
| `getCrewInvites`     		| None       | Get invitation from other crews.                       |
| `getBlockStatus`      	| None       | Checks if blocking friend request is on or off         |
| `getProfile`          	| None       | Checks if your profile is private or not               |
| `getCampaigns`        	| None       | Get all campaigns.                                     |
| `getMails`            	| None       | Get messages from friends.                             |
| `getNotifications`    	| None       | Get notifications from news.                           |
| `getNews`             	| `""`       | Get the news from EE.                                  |
| `checkUsername`    		| `Nickname` | Check if the nickname is already registered 			  |




### Send Information
| Command               | Parameters            | Description
| ------                | ----------            | -----------                                            |
| `createCrew`          | `CrewName`            | Create a new crew.                                     |
| `changeSmiley`        | `SmileyID`            | Change your smiley.                                    |
| `changeAura`          | `AuraID`,`AuraColor`  | Change your aura and aura color.                       |
| `changeBadge`         | `BadgeId`             | Change your badge.                                     |
| `toggleProfile`       | `Boolean`             | Toggle your profile. Show or Hide.                     |
| `blockAllInvites`     | `Boolean`             | Toggle your friend invitation. On or Off.              |
| `deleteFriend`        | `Nickname`            | Delete a friend.                                       |
| `deleteInvite`        | `Nickname`            | Delete invitation from a friend.                       |
| `createInvite`        | `Nickname`            | Send a friend request to the user.                     |
| `answerInvite`        | `Nickname`,`Boolean`  | Accept or decline the friend request.                  |
| `blockUserInvites`    | `Nickname`,`Boolean`  | Block friend requests from the user or not.            |
| `sendMail`            | `Nickname`,`Subject`,`Message`  | Send a message to your friend.               |
| `deleteMail`          | `Key`                 | Delete a message from your friend.                     |
| `blockCrewInvites`    | `CrewID`,`Boolean`    | Block invites from a crew.                             |
| `dismissNotification` | `CrewID`              | Block notifications from a crew.                       |
| `useEnergy`           | `EnergyToSpend`,`Object`| Spend x energy on the object.                        |
| `useAllEnergy`        | `Object`                | Spend all energy on the object.                      |
| `useGems`             | `GemsToSpend`,`Object`  | Spend gems on the object.                            |
| `setUsername`         | `Nickname`              | Set your nickname on your new account.               |
| `changeUsername`      | `Nickname`              | Change your nickname to a new one.                   |
| `acceptTerms`         | None                    | Accept the EE terms.                                 |

## Get information from getShop
Occurs when you send getShop in Lobby.

| Id   | Type        | Name               | Description
| ---  | ---         | ----               | -----------
| `1`  | `Integer`   | Energy             | Your current energy.
| `2`  | `Integer`   | Time till Energy   | Time till you get more energy.
| `3`  | `Integer`   | Total Enegy        | Your total energy.
| `4`  | `Integer`   | Seconds            | Seconds between energy.
| `...`  | `...`     | ...           	  | Loop through the shop from Integer 5, and increase by Integer 25.
| `1`  | `String`    | Id            	  | The id of the item. Example: brickdiamond.
| `2`  | `String`    | Type            	  | The type of the item.
| `3`  | `Integer`   | Energy Price       | How much the item cost in energy.
| `4`  | `Integer`   | Energy Price times | How many times you need to use energy to obtain the item.
| `5`  | `Integer`   | Energy Used 		  | How much energy you have used on the item.
| `6`  | `Integer`   | Gem Price		  | How much the item cost in gems.
| `7`  | `Integer`   | Owned Count		  | How many items you have of this type.
| `8`  | `Integer`   | Span		  		  | Unknown
| `9`  | `String`    | Text Header		  | Text Header.
| `10`  | `String`   | Text Body	      | Text Body.
| `11`  | `String`   | Tab ID	     	  | The tab id in the shopmenu in the EE client.
| `12`  | `Integer`  | Tab Offset	      | The tab position in the shopmenu in the EE client.
| `13`  | `Boolean`  | Is on Sale	      | If the item is on sale.
| `14`  | `Boolean`  | Is Featured	      | If the item is featured.
| `15`  | `Boolean`  | Is Classic	      | If the item is classic.
| `16`  | `Boolean`  | Is Owner Only	  | If the item can only be used in your own world.
| `17`  | `Boolean`  | Is New	  		  | If the item is new.
| `18`  | `Boolean`  | Is Developer Only  | If the item can only be used by developers.
| `19`  | `Boolean`  | Is Grid Featured   | Unknown
| `20`  | `Integer`  | The price in usd   | How much the item cost in USD.
| `21`  | `Boolean`  | Can be reusable    | If the item can be reusable.
| `22`  | `Integer`  | Max Purchases      | If the item can only be bought x times.
| `23`  | `Boolean`  | Owned in PayVault  | If the item is owned in PayVault.
| `24`  | `String`   | Text Label         | The text label of the item.
| `25`  | `String`   | Text Label Color   | The color of the text label of the item.

## Get information from getMySimplePlayerObject
Occurs when you send getMySimplePlayerObject in Lobby. 
When finished looping through ss and se you would get the count for the start of PlayerObject data.  
Just increase from the ss and se total count, and you will get the data. I just list the different types from 0 to 30.  

| Id   | Type        | Name               | Description
| ---  | ---         | ----               | -----------
| `..` | `String`    | ss     			  | The first message of Settings.
| `..` | `..`    	 | Data     		  | The different Settings.
| `..` | `String`    | se     			  | The last message of Settings.
| `0`  | `String`    | Nickname     	  | The nickname you use.
| `1`  | `Integer`   | Smiley     	  	  | The smiley that you use.
| `2`  | `Integer`   | Aura     	  	  | The aura that you use.
| `3`  | `Integer`   | AuraColor    	  | The aura color that you use.
| `4`  | `Boolean`   | Chat Banned    	  | If you are chat banned.
| `5`  | `Boolean`   | Can Chat    	      | If you can chat.
| `6`  | `Boolean`   | Have Smiley Package| If you have the smiley package.
| `7`  | `Boolean`   | Is Administrator   | If you is Administrator.
| `8`  | `Boolean`   | Is Mod   	      | If you is Moderator.
| `9`  | `Boolean`   | Gold Member    	  | If you is Gold Member.
| `10` | `Boolean`   | Wears Gold Smiley  | If you use a gold smiley.
| `11`  | `Number`   | Gold Remain    	  | How long time you can use gold member.
| `12`  | `Number`   | Gold Time   	  	  | ^ I don't know.
| `13`  | `Boolean`  | Gold Welcome   	  | Welcome message for gold members I guess.
| `14`  | `String`   | room0              | Your first nonbeta world, when you was a beta tester.
| `15`  | `String`   | Beta Only Room     | Your first beta world.
| `16`  | `String`   | Home World     	  | Your home world.
| `17`  | `String`   | Size of worlds     | The size of all your worlds. Split it with (char)0x1399.
| `18`  | `String`   | WorldID of worlds  | The WorldID of all your worlds. Split it with (char)0x1399.
| `19`  | `String`   | Names of worlds    | The names of all your worlds. Split it with (char)0x1399.
| `20`  | `Boolean`  | Visible     	      | If your profile is set to be visible or not.
| `21`  | `Boolean`  | Banned     	      | If you are banned from EE or not.
| `22`  | `Integer`  | Accepted Terms     | If you have accepted EE rules.
| `23`  | `String`   | Badge     	  	  | Your badge that you use.
| `24`  | `Boolean`  | Confirmed Email    | If you have confirmed your email, maybe postman.
| `25`  | `Integer`  | Max Energy    	  | The max energy you have.
| `26`  | `Boolean`  | Change Name    	  | If you have changed your name.
| `27`  | `String`   | WorldIDs from favorites | The worldid of your favorites. Split it with (char)0x1399.
| `28`  | `String`   | World Name from favorites | The world name of your favorites. Split it with (char)0x1399.
| `29`  | `Boolean`  | Is Staff    	      | If you belong to the staff.
| `30`  | `Boolean`  | Universe    	      | If you have joined EEU Beta.

