# Tiers Plugin Commission

### **What is the Tiers System?**
The tiers system is a simple system in which allows players to level up specific items (Coal, Rotten Flesh, etc) by completeing requirements. In return, they get a higher sell bonus of the item the higher level they are.

There are three different "categories":
* Slaying -> Show all mobs -> Each mob has it's own GUI
* Mining
* Farming
Each categories organise items so the items aren't in one GUI. 

The system is also island based, and should use the SuperiorSkyblockAPI, which means all data is island-based. Remember that the categories only seperate items, so if there were two coal items, both in the Slaying and Mining, the data would be synced between them. 

The system is hard to understand at first for many, so let's introduce an example:<br>
Let's say we have a carrot. All items start at Level I (0% sell bonus), so if I were to sell the carrot right now, it would be the same price as in the Shop. Now, let's say to get to Level II, the requirement is to harvest 6000 carrots, while I do that, it should bump up the counter in the GUI, and once I finish, I can click the item to upgrade to level 3.

### **The Requirement System**
The requirement system is based off the SuperiorSkyblock mission system, where you put jars in a specific folder and the plugin itself loads those jars. The jars manage all the tracking, checks, etc. for that requirement. This is a more ideal system due to the fact that we will add more requirements ourself as the season goes on without having to directly edit the source or making a seperate plugin for it. For this commission, we would like four to be done:
* Harvest
* Kill Mob
* Collect Item
* Mine Block

For example, in the "requirements" folder, you would have all the requirement jars. 
Each jar will have it's own settings, which is editable in the main `requirements.yml` configuration, under the "type-settings", the "type" would be the name of the jar without the .jar.

```
requirement:
  type: 'Mine'
  type-settings:
    mine-block: COAL_ORE
    mine-data: 0
    mine-amount: 1000
```
### Skip Tokens
Skip Tokens are tokens that will be used to skip a certain level on a certain item. To redeem this, they would right click the item they would want to skip a level on with the skip token in their inventory.

### Pictures
The system is a bit hard to understand at first! Pictures will really help you understand the system more. 

https://youtu.be/3PVZ8-JL6ck<br><br>
![](https://i.intriguing.me/images/2020/07/02/javaw_PFbK6uxrZG.png)
![](https://i.intriguing.me/images/2020/07/02/javaw_X7o13FJeP5.png)

### Notes
Commands:
/tiers - Open GUI<br>
/tiers set <PLAYER> <ITEM> <LEVEL> - Set user to specific level<br>
/tiers reload - Reload Configurations<br>
/tiers givetoken <PLAYER> <AMOUNT> - Give token to user.

- Hooks: ShopGUIPlus + SuperiorSkyblock2
- There should be fallback menus (e.g. if I hit ESC on the Slaying menu, it should bring me back to the Main Menu
- MySQL option available. 
