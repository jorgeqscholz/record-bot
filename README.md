# DecisionBot

DecisionBot is a Reddit bot that retrieves and posts martial arts scorecards on-demand. It is triggered when users comment in any [r/mma](https://www.reddit.com/r/mma) thread with the fighter names.

* [Example of use in discussion](https://www.reddit.com/r/MMA/comments/5zh47e/name_a_brutally_honest_fact_about_a_fighter_that/dey9kac/?context=3)
* [Various usage examples](https://www.reddit.com/r/bottesting/comments/606f58/decisionbot_usage_examples/)
* [Initial release thread on r/mma](https://www.reddit.com/r/MMA/comments/5vy9cc/decisionbot_new_rmma_bot_that_posts_decision/)

# Usage example
* User leaves comment: **decisionbot mcgregor vs diaz**
* DecisionBot replies:

    ### [**CONOR MCGREGOR defeats NATE DIAZ** (*majority decision*)](http://mmadecisions.com/decision/7244/fight)

    UFC 202: Diaz vs. McGregor 2 — August 20, 2016

    ROUND|McGregor|Diaz| |McGregor|Diaz| |McGregor|Diaz
    :-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:
    1|10|9| |10|9| |10|9
    2|10|9| |10|9| |10|9
    3|9|10| |9|10| |8|10
    4|10|9| |10|9| |10|9
    5|9|10| |9|10| |9|10
    **TOTAL**|**48**|**47**| |**48**|**47**| |**47**|**47**

    *Judges, in order: Derek Cleary, Jeff Mullen, Glenn Trowbridge.*

    **MEDIA MEMBER SCORES**

    * **1/19** people scored it **49-47 McGregor**.
    * **12/19** people scored it **48-47 McGregor**.
    * **1/19** people scored it **47-46 McGregor**.
    * **4/19** people scored it **47-47 DRAW**.
    * **1/19** people scored it **47-48 Diaz**.

# Features
* You can use v / v. / vs / vs. / versus, or leave it out and the bot will figure it out.
* Handles rematches (include the rematch number in the comment, or leave it out and the bot posts all fights).
* Handles many fighter nicknames and common name misspellings.
* Comments are not case-sensitive.
* Put "decisionbot" anywhere in your comment.
* Includes several easter eggs.

# Files
File|Description
:-:|---
*fight_finder.py*|Searches and pulls fight data from [mmadecisions.com](http://mmadecisions.com/) using [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/).
*decision_bot.py*|Runs the bot on Reddit.
*notify_account.py*|Notifies my personal account of DecisionBot's status.
Bash scripts|Used for running DecisionBot continuously on server.
*config.yaml*|Various configurations in YAML format.
*commented.txt*|List of recent comments that triggered DecisionBot.
*nicknames.txt*|List of common nicknames and name misspellings.
*rematches.txt*|Correctly adjusted rematch numbers.
