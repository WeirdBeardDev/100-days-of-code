# Daily Game Design and Development Log
**Log Repo:** [WBD 100 Days of Code](https://github.com/WeirdBeardDev/100-days-of-code)

## Day 1 - 2019.10.27
**Project:** Treasure Hunter: Quixxen's Suit (formerly Dungeon Explorer)
I began working on my game again.  I reviewed the design for the Adventurers and realized it was crap, so I scraped it and started over.  This time I will design, code, and test in smaller cycles so that I don't create a mess of useless code that I will have to massively refactor later.

This is my first game project, I don't need it perfect, I need it workable so I can learn and improve.

### Commits
* commit `be0e8de` - Started Overhauling Skills 
  * gutted the Skill class and redefined to bare essentials, I plan to build it back up by using it
  * refactored GrantIncomeSkill to match new Skill base

* commit `e79e6e1` - Added Formulas and LeveledFloat Classes 
  * added Formulas static class to feed into the LeveledFloat class
  * added a LeveledFloat class which levels up the cost and output based upon formulas for use in incremental games

* commit `22ba643` - Fixed Bug In Stat Class
  * refactored BaseValue to return just the base value

* commit `a9deb4d` - Refactored Quest Income To Use Stat Class
  * fixed bug in Stat where changing BaseValue would not trigger a recalc
  * renamed Stat.Value to Stat.CalculatedValue to improve readability
  * refactored Quest.CurrentExperience into simple auto-property definition
  * refactored Quest.IncomePerSecond to use Stat
  * refactored IncomeGoal.AssessGoal to use Stat IncomePerSecond
  * refactored WorkdingQuest to use Stat IncomePerSecond
  * refacotred DisplayQuest to use Stat IncomePerSecond

* commit `b5189aa` - Renamed Trait to Stat
  * Changed all Trait related names to Stat