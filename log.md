# 100 Days Of Code - Log
**Log Repo:** [WBD 100 Days of Code](https://github.com/WeirdBeardDev/100-days-of-code)

## Day 24 - 2019.09.15
**Project:** Dungeon Explorer (codename)
* Spent about 25 mins fighting with VS Code which isn't opening my Unity files any more no matter what I try
* Finally got the project open in Visual Studio 2017 only to find out that it is no longer saving or loading at all
* Spent the last 35 minutes trying to figure out WTF and can't
* Sometimes this is what coding looks like

## Day 23 - 2019.09.14
**Project:** Dungeon Explorer (codename)
* commit `5502696` - Basic Load Game Functionality Implemented
  - coded LoadHelper in GameManager to resetup the game
  - coded LoadData in QuestZoneDetails
  - refactored Awake and Start in QuestZoneDetails to streamline setup

## Day 22 - 2019.09.13
**Project:** Dungeon Explorer (codename)
* commit `e50c13d` - Renamed SaveZoneData To SaveData
  - renamed class it will encompass all the game state for the game not just the zones
* commit `3ea9161` - Saving/Loading From File Works
  - coded LoadGame() in GameManager
  - fixed bug in QuestZoneDetails where List<Quest> was not initialized by property
  - coded LoadGame() in GameFile to deserialize the object back in
  - currently the object is loaded in memory only, next step is to get it applied to the game state

## Day 21 - 2019.09.12
**Project:** Dungeon Explorer (codename)
* commit `386cb5f` - Working On Saving Data 
  - refactored GameMaager to get zone details and setup the save object
  - added a temp Save button to test my save code
  - refactored QuestZoneDetails to connect to GameManager so GM records came state but the zone manages itself
  - removed Current and AllTime experience totals as they aren't needed at the encounter level
  - renamed QuestZoneData to SaveZoneData
  - coded a temp SaveAsJson method in GameFile, managed to get some of my data saved, however, lists are not working

## Day 20 - 2019.09.11
**Project:** Dungeon Explorer (codename)
* commit `0b931f75` - Working On Serializing Classes
  - refactored Encounter for serializing and removed unneeded code
  - refactored EncounterType, Goal, IncomeGoal, ForestQuest, PlainsQuest, Quest, QuestZoneType, RiversQuest for serializing
  - refactored DisplayQuest to align with new Encounter updates
  - refactored GameFile so fileName is readonly

## Day 19 - 2019.09.10
**Project:** Dungeon Explorer (codename)
* commit `062ac91` - Starting the Save/Load Game Changes
  - refactored DisplayQuest to remove members
  - refactored QuestZoneDetails adding and removing members to support saving/loading
  - refactored WorkingQuest to remove ref to button
  - coded QuestZoneData class to save all the data for each quest zone
  - refactored ForestQuest and RiverQuest to detail to their respective zone types
  - coded GameFile class to do the saving and loading of the game file

## Day 18 - 2019.09.09
**Project:** Dungeon Explorer (codename)
* commit `02e5ce1` - Code Ability To Instantiate Quests
  - created QuestFactory to return correct type of quest object
  - refactored Quest Location prefab to ref its own button
  - refactored Quest Zone prefab to apply changes for displaying quests correctly
  - removed unused code from GameManager
  - refactored QuestZoneDetails to instantiate quests as needed
  - refactored WorkingQuest simplifying the code
  - updated doc in Quest
* Non-code Activities
  * published [DE Devblog 5 - Uncharted Territory](https://weirdbearddev.com/?p=597) to [WBD](https://weirdbearddev.com), [Twitter](https://twitter.com/weirdbearddev/status/1171267951816785922), [r/devblogs](https://www.reddit.com/r/devblogs/comments/d227tr/dungeon_explorer_devblog_5_uncharted_territory/), [PixelFest Devs](https://www.facebook.com/groups/1738572983081896/permalink/2453730131566174/) 

## Day 17 - 2019.09.08
**Project:** Dungeon Explorer (codename)
* commit `13d25ca` - Improving QuestZoneDetails To Manage Each Zone
  - QuestZoneDetails maintains a List<Quest> for it's zone
  - wired up the temp creation of specific Quest types; will convert to factory in future
  - in WorkingQuest exposed public properties ActiveQuest to receive input from QuestZoneDetails
* commit `46cb3da` - Improved Singleton and GameManager 
  - added checks for is quitting and to return null if quitting
  - added a lock for thread safety
  - updated GameManager.OnApplicationQuit to call the base class

## Day 16 - 2019.09.07
**Project:** Dungeon Explorer (codename)
* commit `ae27573` - Zone Names Come From Enum
  - added the QuestZoneType enum to the QuestZoneDetails so the name is set from the enum
* commit `3788367` - Create Singleton<T> and GameManager
  - created a base Singleton<T> class to ensure all singletons are created the same
  - refactored GameManager to derive from Singleton<T>
  - added an InitializeGame() to GameManager
  - added a QuitGame() to GameManager
* commit `aebd8db` - Fixed Missing Text in Plains Quest 
  - updated text for names
  - added some missing action text
* Non-code Activities
  * Posted [Write Code, Wrong Branch](https://weirdbearddev.com/2019/09/07/write-code-wrong-branch/) to WBD and Twitter

## Day 15 - 2019.09.06
**Project:** Dungeon Explorer (codename)
* commit `8f4cf58` - Worked on GameManager 
  - created GameManager class and stated moving code to it
  - refactored WorkingQuest to use GameManager
  - refactored Quest base class
  - refactored PlainsQuest and ForestQuest classes to match new Quest base
  - coded RiversQuest class as it is the second zone
  - refactored Encounter with UpdateNameAndActionText to go with updated Quest
  - created enum QuestZoneType to list all 12 zones and remove magic numbers
  - removed ContentCounter class as it is not needed, a list of Quests is kept at the zone level
  - refactored QuestZoneDetails to remove ContentCounter dependency
  - renamed 'Quest Loction' to 'Quest Location', missed an 'a' originally
* Non-code activities
  * Posted [DE devblog 2](https://ko-fi.com/post/Dungeon-Explorer-Devblog-2---Start-Your-Coding-M4M512XIE) to Ko-fi
  * Posted [Trello - The All-Purpose Holder of Things](https://ko-fi.com/post/Trello---The-All-Purpose-Holder-of-Things-U7U812XJ5) to Ko-fi
  * Posted [DE devblog 3](https://ko-fi.com/post/Dungeon-Explorer-Devblog-3---Progress-on-Progress-Z8Z412XJI) to Ko-fi
  * Posted a [WIP progress bar](https://az743702.vo.msecnd.net/cdn/useruploads/post/gif_kofi_bbd8724e-5a17-4308-b447-7d77bbc6e179progressbar2.gif) to Ko-fi

## Day 14 - 2019.09.05
**Project:** Dungeon Explorer (codename)
* commit `7ea3b9a` - Started GameManager
  - added Game Manager to hierarchy
  - created and added GameManager script to Game Manager
* updated VS Code to v1.38 August 2019
* created new branch GameManager-A
* merged QuestBoard branch onto master
* commit `c0458cc` - Removed Test Quests
  - alpha tests passed, removed test quests, saved scene

## Day 13 - 2019.09.04
**Project:** Dungeon Explorer (codename)
* commit `a011f7b` - Fixed Bug in ContentCounter
  - It now updates the count when it changes
* commit `5f12984` - Quest Zone Details Are Configurable
  - Added a formatted title "{Active Quests} {Title} Zone"
  - Added ability to update zone title
  - Refactored ContentCounter to expose the current count
* commit `39e78f5` - Added Scrollbar Functionality to QuestBoard Title
  - Got the mouse wheel working, I needed to change the sensitivity
  - Coded ability to scroll through zones while hoving over quest board title
* commit `0121c10` - Added All 12 Zones to Quest Board
  - Updated Quest Zone prefab to include a quest counter
  - Added all 12 quest zones to the quest board, updated names
  - Tweaked DisplayQuest so it no longer spams console when no quest is selected
* commit `b6a5ab5` - Updated Encounter Sheet
  - Added in line work for puzzle and trap encounters
  - Removed LocationIcons file as it's no longer needed
* Non-code activities
  - updated [WeirdBeardDev Ko-fi page](https://ko-fi.com/weirdbearddev) with catch-up posts for DE
  - created an album for DE and uploaded WIP art

## Day 12 - 2019.09.03
**Project:** Dungeon Explorer (codename)
* commit `bff7655` - Created Quest Location Prefab
  - removed unused Change Quest prefab
  - created Quest Location prefab with Progress Bar
  - added Quest Location prefabs to Forest Quest Zone for testing
  - applied WorkingQuest script to Quest Location prefab
  - coded the progress bar to reflect goal progress for it's quest

## Day 11 - 2019.09.02
**Project:** Dungeon Explorer (codename)

* learned how to use `git stash` to move changes from one branch to another

Commits done to branch `QuestBoard`
* commit `512c7c2` - Turned ProgressBar Indicators On
  - I had turned off the progress bar indicators for screenshots
* commit `09130fa` - Created QuestBoard Feature Branch 
  - Updated QuestBoard area with needed game elements
  - Created Quest Zone prefab, added 3 for testing purposes

Commits done to branch `QuestArea`
* commit `a2aeb9b` - merged `QuestArea` to `master`, pushed to `origin`

## Day 10 - 2019.09.01
**Project:** Dungeon Explorer (codename)

All commits done to local branch `QuestArea`
* commit `a2aeb9b` - Fixed Background Processing 
  - Fixed bug so that a quest continues even if it isn't selected
  - Refactored DisplayQuest to use less Find(...) calls
  - Update IncomeGoal to make easier to test


## Day 9 - 2019.08.31
**Project:** Dungeon Explorer (codename)

All commits done to local branch `QuestArea`
* commit `a0efc861` - Goal Assessment Implemented
  * Coded abstract Goal class
  * Coded IncomeGoal class
  * Added Goal Button to DisplayQuest
  * Goal Button displays Quest progress towards goal
  * Changed Encounter.IncreaseCost temp formula to make it easier to test
  * Added Zone to Quest so formulas can change based on quest zone

## Day 8 - 2019.08.30
**Project:** Dungeon Explorer (codename)

All commits done to local branch `QuestArea`
* commit `fc9ecc8` Buy Encounter Done & Button Highlighting Coded
  * Buying an encounter now adds the benefit and subtracts the cost
  * Quest updates the AllTimeExperience and CurrentExperience correctly
  * PurchasableEncounter script coded to change Button coloring based on interactable/non-interactable status


## Day 7 - 2019.08.29
**Project:** Dungeon Explorer (codename)

All commits done to local branch `QuestArea`

* commit `f414054` Basic Purchase Almost Complete
  * Changed DisplayQuest to call Quest.DoEncounter()
  * Add Quest.DoEncounter() to call Encounter.DoEncounter()
  * Wired up Income Per Second and Available XP
  * Coded purchasing of encounters for benefits - cost is evaluated but not subtracted yet
* commit `d463fe1` Update Encounter Sprites
  * added sprite sheet EncounterSheet1
  * set images for the 4 fight encounter types

## Day 6 - 2019.08.28
**Project:** Dungeon Explorer (codename)

All commits done to local branch `QuestArea`
* commit `bc56c4b` Saved the Scene
* commit `7d789de` Created Income Display Prefab
* commit `9710a58` Fixed a Bug in DisplayQuest
  * added a null check to DoEncounter()
* commit `d11e8e2` Encounter Button Completes the Encounter
  * Class: `DisplayQuest`
    * EncounterButton calls the correct Encounter and completes it
    * I have basic functionality to increase completed and adjusted cost.
    * Changed the Update() method to only update when something has changed.
    * Added methods for Display* {Title|Income|Encounter|Goal}.
    * Coded the DisplayTitle method
  * Encounter
    * I changed the IncomePerSecond to return just the income, not the sum of all previous incomes.
    * I created AggregateIncome to return the sum of all income adjustments.

## Day 5 - 2019.08.27
**Project:** Dungeon Explorer (codename)

All commits done to local branch `QuestArea`
* commit `a5a5ce3` Wired up Encounter Buttons - the correct encounter number is displayed in console
* commit `9cdc91f` Minor Tweak To Encounter Button Setup - condensed two lines into one

## Day 4 - 2019.08.26
**Project:** Dungeon Explorer (codename)

All commits done to local branch `QuestArea`
* commit `da53411` Changed Encounter Button to ButtonProgressBar to support the Autobuy feature in the future
* commit `c14071c` Fixed Bug in Encounter\Do Encounter\Button\Action Text so it updates with the rest of the UpdatableText items

## Day 3 - 2019.08.25
**Project:** Dungeon Explorer (codename)

All commits done to local branch `QuestArea`
* commit `f09e890` Updated ProgressBar code so I can easily update FillColor and ForegroundSprite image
* commit `e62b2a9` Added ButtonProgressBar Code - now it has similar functionality as the ProgressBar
* commit `d54da40` Fixed ProgressBar OnCompleted Not Firing - was only firing if the current value > the max value, now it fires correctly with when the current value >= max value

## Day 2 - 2019.08.24
**Project:** Dungeon Explorer (codename)
* local branch `QuestArea` commit `d896bc5` - Fixed ProgressBar not scaling when resizing
* local branch `QuestArea` commit `5514560` - Created a prefab for the ButtonProgressBar

## Day 1 - 2019.08.23
I [tweeted](https://twitter.com/weirdbearddev/status/1164876725521661957) my start, and now to write code.

### Progress Made
**Project:** Dungeon Explorer (codename)
* local branch `QuestArea` commit `bb8b674` - Started dev on progress bar
* local branch `QuestArea` commit `a355825` - Stopped Unity's warning about unused private fields
* local branch `QuestArea` commit `50461b8` - Copied over ProgressBar code
