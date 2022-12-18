# Privacy Policy 
## 0) Overview

In the following you’ll learn all about data storage/use/deletion within the Booty-bot-Project. 
The bot was mainly developed by Tratos#5673
All points will start with a summary and go into more detail afterwards


## 1) What data is collected?
Booty, by default, stores as little data as possible. To be more specific, he always stores exactly 3 things: 

A) The server ID
B) One member ID per user
C) One timestamp* per user
* this timestamp will be overwritten when a user participates on your server

### 1.2 Optional - This data will be stored seperately if members are whitelisted - 
(whitelisted = excluded from all kicks)

A) The server ID (again)
B) User/member IDs of whitelisted people

### 1.3 Possibly with future updates:
C) A boolean value*
* for non programmers, this is a tiny information representing a simple True or False statement
D) Information about role(s) on your server 
 
It is also possible, that the bot needs other data for functions not planed by the time this privacy policy is written. 
IF that happens or any of the ideas in 1.3 get implemented it will be pronounced here as well as in Bootys’ video comments, as a pinned comment, at least 4 weeks before the new features are rolled out:
[Bootys' video](https://www.youtube.com/watch?v=6e8Y9NaIzfk)
  
From a development point of view, it would be more convenient to simply store the user objects, as they are required to give kick orders. However, since Booty was designed to store as little data as possible, 
the decision was made only to call on, and not store, the user object that is required to kick a member. This was achieved at the cost of lengthening Booty's code and making it a bit less convenient to work with. 

## 2) Where is the data coming from?
 Discord-API: The API helps to collect data from Discord
→ https://discord.com/developers/docs/intro
Pythons’ Datetime-library. The Bot generates a timestamp when he sees user activity.
Commands: Some comments (e.g. whitelist_add) provide information for the bot. 
→ https://www.remote.tools/remote-work/discord-commands






## 3) What is the data used for?
The data is needed because Booty's main purpose is to track the participation of members on your server. 
It allows the bot to kick members that have not participated on the server for a given number of days, which can be defined by the server owner and the users he/she has granted access to Booty's slash commands. 

Some data is stored to prohibit kicking certain people. 
Data will never be used for any purpose other than Bootys’ functionallity and development.

## 4) Data access
Users have access to the data associate with their own Discord-Server. 
Only Booty's developers have access to the entire database. This data will not be shared with any third party for any reason. 

## 5) Contact
If you have any questions about Booty, feel free to join his support-Discord

[Join the support-Discord](https://discord.gg/kE4s84bRmD)

And yes, you are allowed to ping me (=Tratos) if your request is urgent or you did not recieve an answer within a couple of days. 


## 6) Deleting data 
As stated in Booties’ video:
[Bootys' video](https://www.youtube.com/watch?v=6e8Y9NaIzfk)
you should inform people about Booty before they join your Discord (it’s recommended to write about him in your server rules). 
However sometimes people did not read them closely or change their mind later. 

What ever the reason, here is how Booty’s data gets deleted:

If a user is no longer part of your server, simply run the /update_db command. The bot will notice he or she is gone and delet the entry from its database automatically. 

In case you want your entire server and all related data to be removed from its database simply kick the bot!
He will notice that he is no longer on this server and delete everything within 14 days. 

It is not possible to use Booty and have members who do not want to be stored. In this case you need to remove the bot. (please read on)

Originally we wanted to make Booty opt-in, but had to decide against it. It’s core function is to remove inactive users. 
Inactive users will not opt-in (or do anything really :D) and their data won’t be stored after they were kicked and /update_db was used. 
Therefore it has to be this way unless we come up with a better solution, that does not cripple Booties purpose. 

Any timestamp, that is stored for a user, will be overwritten when this user sends a message or joins a voice room, but Booty will not know what the activity was or any of its contents. 
It will only know when a member was last active and will not store a history. 
