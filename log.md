# 100 Days Of Code - Log
**Log Repo:** [WBD 100 Days of Code](https://github.com/WeirdBeardDev/100-days-of-code)

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
