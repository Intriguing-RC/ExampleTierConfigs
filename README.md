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
