# 100 Days Of Code - Log

**[Goals for the 100 days](#day-0)**

|Day|Focus|Day|Focus|
|:---:|:-----:|:---:|:-----:|
|[Day 1](#day-1) **05/18/2020**|Integrate with external API|[Day 2](#day-2) **05/19/2020**|Continue with integrating external API|
|[Day 3](#day-3) **05/20/2020**|Research making API authorization long lived|[Day 4](#day-4) **05/21/2020**|Complete initial integration with external API|
|[Day 5](#day-5) **05/23/2020**|Obtain notes|[Day 6](#day-6) **05/24/2020**|Create DB|
|[Day 7](#day-7) **05/25/2020**|Hook up to MySQL|[Day 8](#day-8) **05/27/2020**|Initial Parsing of Notes|

----------

<a name="day-0"></a>
### Day 0: May 17, 2020

**Today's Focus**: Goals Brainstorming

**Progress**:

- Ideas for what kind of projects / goals I would like to accomplish during this challenge:
  - Ultimate goal is to improve on overall skill set in terms of designing the code and getting faster at it - in the C# language and Javascript
  - Work on some neat interactive JS solutions - perhaps some taken from here https://javascript30.com/
  - Develop a simple game by starting with some activities here: https://www.codingame.com/
    - Possible tutorials to do?: 
      - https://www.codementor.io/@dewetvanthomas/tutorial-game-loop-for-c-128ovxgrig
      - https://www.youtube.com/watch?v=XOJErrCyt5A&vl=de
  - Brush up on algorithms by doing some coding interview questions: 
    - either from the Cracking the coding interview 
    - or doing some from https://leetcode.com/ (https://leetcode.com/explore/other/card/30-day-leetcoding-challenge)
  - more simple coding project ideas? https://www.reddit.com/r/learnprogramming/comments/2a9ygh/1000_beginner_programming_projects_xpost/??
  - work on wallite app?
  - work on new resources site idea?
  - learn how to use unity?

- Brainstorm Session Conclusion:
  - Decided to start with working the resources project that I have been thinking about recently. 
    - I wanted to create something that I would use on a daily basis, and that other people might find useful too, so this resources project meets both criteria.
    - started thinking about possible names to call the site
    - made a simple wireframe (on paper) of what the site could look like
    - decided on using React for the frontend instead of using Razor pages to try it out in ASP.NET Core

<a name="day-1"></a>
### Day 1: May 18, 2020

**Today's Focus**: Integrate with external API

**Progress**: 

- Tried hooking up a quick console app to work with external API unsuccessfully. For some reason the console app launches on a random port, which the external API cannot authenticate with because the port is not a valid redirect URL
- Need to troubleshoot more tomorrow

**Links to work**: None for today as just testing with a console app for now

<a name="day-2"></a>
### Day 2: May 19, 2020

**Today's Focus**: Continue with integrating external API

**Progress**: 

- Got the console app to hook up to the external API directly. All that had to be done was assign the return url with no port number... which was not documented in the docs... :(
- Started integrating external service to resources app

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/eb0b8a3a374c60c1b457353ff769f6639fdfba64)

<a name="day-3"></a>
### Day 3: May 20, 2020

**Today's Focus**: Researched how to make authorization long lived with the external API

**Progress**: 

- Found there is possibility to use API keys instead of OAuth
- Continued to integrate external service to resources app

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/05d7b68ac580cc1338948828c171dc560b713a56)

<a name="day-4"></a>
### Day 4: May 21, 2020

**Today's Focus**: Complete initial integration with external API

**Progress**: 

- Got external API quickstart integrated into Startup and registered with my own service and it works
- May not be able to use API keys after all, seems like API keys are for another service and not for the one I'm integrating with. Still need to look more into this

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/baca35fbe65272b1940cf21dbc2f90354ab8db19)

<a name="day-5"></a>
### Day 5: May 23, 2020

**Today's Focus**: Obtain notes

**Progress**: 

- Dug through the docs and definitely cannot use API keys, because API keys do not allow accessing private data. They are only used to discover other apis the external service has
- Added support to get messageIds and fetch notes (initial implementation, still needs a lot of work (see todos in code))

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/1868b7a6224cb19f7bd079b37f0b97a1a8774e30)

**Todo Tomorrow**:

- Look at Message object in DB to decide which parts are useful to save in the DB
- Add mysql DB and create schema and tables through migrations

<a name="day-6"></a>
### Day 6: May 24, 2020

**Today's Focus**: Create DB

**Progress**: 

- Didn't get very far in creating the DB, but instead got side-tracked and started looking at hosting providers. Maybe will dockerize the project and host it on a VPS instead of using a shared hosting service...
- For the notes, will likely store subject and any disclaimers in the DB

**Links to work**: None today as mostly research

**Todo Tomorrow**:

- Add mysql DB and create schema and tables through migrations

<a name="day-7"></a>
### Day 7: May 25, 2020

**Today's Focus**: Hook up MySQL

**Progress**: 

- Decided between MySQL or MSSQL. Will use MySQL since community edition is free for production use. Might release resources site to the public
- Installed mysql server to local machine
- Added class entities and configuration to DB context

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/3f08161fa02af9b66d24a3844dba5c0777374453)

**Todo Tomorrow**:

- Generate migrations for entities

<a name="day-8"></a>
### Day 8: May 27, 2020

**Today's Focus**: Initial Parsing of Notes

**Progress**: 

- Studied what the notes objects returns and determined which fields can be parsed and saved to the database

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/b1022f8eceaf866c5245cad1f3fc6b340c3c4fb2)

**Todo Tomorrow**:

- Write parsers for different kinds of notes
- Add the brand name to the note db


<!--
template

<a name="day-"></a>
### Day : May , 2020

**Today's Focus**: 

**Progress**: 

- 

**Links to work**: [resources]()

**Todo Tomorrow**:

- 


-----



**Today's Progress**: Fixed CSS, worked on canvas functionality for the app.

**Thoughts:** I really struggled with CSS, but, overall, I feel like I am slowly getting better at it. Canvas is still new for me, but I managed to figure out some basic functionality.

**Link to work:** [Calculator App](http://www.example.com)

### Day 0: February 30, 2016 (Example 2)
##### (delete me or comment me out)

**Today's Progress**: Fixed CSS, worked on canvas functionality for the app.

**Thoughts**: I really struggled with CSS, but, overall, I feel like I am slowly getting better at it. Canvas is still new for me, but I managed to figure out some basic functionality.

**Link(s) to work**: [Calculator App](http://www.example.com)


### Day 1: June 27, Monday

**Today's Progress**: I've gone through many exercises on FreeCodeCamp.

**Thoughts** I've recently started coding, and it's a great feeling when I finally solve an algorithm challenge after a lot of attempts and hours spent.

**Link(s) to work**
1. [Find the Longest Word in a String](https://www.freecodecamp.com/challenges/find-the-longest-word-in-a-string)
2. [Title Case a Sentence](https://www.freecodecamp.com/challenges/title-case-a-sentence)

-->
