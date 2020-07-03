# 100 Days Of Code - Log

**[Goals for the 100 days](#day-0)**

|Day|Focus|Day|Focus|
|:---:|:-----:|:---:|:-----:|
|[Day 1](#day-1) **05/18/2020**|Integrate with external API|[Day 2](#day-2) **05/19/2020**|Continue with integrating external API|
|[Day 3](#day-3) **05/20/2020**|Research making API authorization long lived|[Day 4](#day-4) **05/21/2020**|Complete initial integration with external API|
|[Day 5](#day-5) **05/23/2020**|Obtain notes|[Day 6](#day-6) **05/24/2020**|Create DB|
|[Day 7](#day-7) **05/25/2020**|Hook up to MySQL|[Day 8](#day-8) **05/27/2020**|Initial Parsing of Notes|
|[Day 9](#day-9) **05/28/2020**|Error With DB Inserts|[Day 10](#day-10) **05/30/2020**|Add Brand Name|
|[Day 11](#day-11) **05/31/2020**|Frontend Work|[Day 12](#day-12) **06/01/2020**|Replaced Frontend|
|[Day 13](#day-13) **06/03/2020**|Fetch Notes from React|[Day 14](#day-14) **06/04/2020**|Display Multiple Notes in UI|
|[Day 15](#day-15) **06/05/2020**|Render HTML Strings|[Day 16](#day-16) **06/06/2020**|Modal State Management|
|[Day 17](#day-17) **06/07/2020**|Add Search Bar|[Day 18](#day-18) **06/08/2020**|Add Search Query|
|[Day 19](#day-19) **06/09/2020**|Add Categories|[Day 20](#day-20) **06/13/2020**|Filter Categories Functionality|
|[Day 21](#day-21) **06/14/2020**|Filter Categories And Search Behaviour|[Day 22](#day-22) **06/16/2020**|Research How to Parse Resource|
|[Day 23](#day-23) **06/20/2020**|Continue Research|[Day 24](#day-24) **06/21/2020**|Added Date Parser|
|[Day 25](#day-25) **06/26/2020**|Algo Arrays|[Day 26](#day-26) **06/27/2020**|Algo Arrays & Resources Add Sort by Ends Filter|
|[Day 27](#day-27) **06/28/2020**|Algo Questions & Resources Show Created & Apply Consistent Sorting|[Day 28](#day-28) **06/30/2020**|Algo Arrays|
|[Day 29](#day-29) **07/01/2020**|Algo Linked Lists|[Day 30](#day-30) **07/02/2020**|Algo Linked Lists|

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
  - Read up on ASP.NET Core and c# topics such as using blocks... what resources need to be disposed of... etc.

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

<a name="day-9"></a>
### Day 9: May 28, 2020

**Today's Focus**: Error With DB Inserts

**Progress**: 

- Seems like trying to insert 100 notes at once into the db is too much. Error suggests maybe out of memory? Didn't dig too far but reduced the load to 50 inserts and this worked
- Added Brands enum
- Added queries to limit the retreival of notes to certain brands

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/1b712e9038aa44f95386e84a3149d769cec925c2)

**Todo Tomorrow**:

- Add the brand name to the note db
- Get the db saved info displayed on the frontend
- Will write parser for different kinds of notes at later date

<a name="day-10"></a>
### Day 10: May 30, 2020

**Today's Focus**: Add Brand Name

**Progress**: 

- Added brand name to the DB
- Wrote separate brand names - one used for queries and one for display, and added conversion methods to convert the two from one type to another 
- Commited initial migration

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/11789d4ec6c55f831790a48442ef3455037c9ba8)

**Todo Tomorrow**:

- Get the db saved info displayed on the frontend

<a name="day-11"></a>
### Day 11: May 31, 2020

**Today's Focus**: Frontend Work

**Progress**: 

- Added API endpoint to retrieve notes
- Removed default frontend files and tried to create new react typescript project, but currently typescript template is broken for CRA... so reverted back just going to modify the existing project to be suitable for the site
- Added initial Resources component

**Links to work**: [Resources Project Commit 1](https://github.com/seshieya/WooDeals/commit/f1b5cbd1ef518ed510c762e0ca363ad8706b91c2),
[Resources Project Commit 2](https://github.com/seshieya/WooDeals/commit/c4c72613e5c06307f6022ddce508f11b71aae512)

**Todo Tomorrow**:

- Clean up react project to use typescript properly and possibly start working on the Resources component

<a name="day-12"></a>
### Day 12: June 1, 2020

**Today's Focus**: Replace Frontend with Empty Typescript CRA

**Progress**: 

- Figured out why typescript template was broken... it was because I had global create react app installed
- Replaced existing frontend with empty typescript CRA

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/2feaff46f9d54f382611acfd61c3d53b21d718d4)

**Todo Tomorrow**:

- Work on the resources component 

<a name="day-13"></a>
### Day 13: June 3, 2020

**Today's Focus**: Fetch Notes from React Frontend

**Progress**: 

- Set up react frontend to fetch notes from API :)

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/834dddd43301b1d3dc37caf1f30542d6cdf3f6f4)

**Todo Tomorrow**:

- Continue working on the resources component

<a name="day-14"></a>
### Day 14: June 4, 2020

**Today's Focus**: Display Multiple Notes in UI

**Progress**: 

- Added reactstrap and made notes appear like a grid and also added modals

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/a09f853c79df735f7dd20aa83be190155e1af9cd)

**Todo Tomorrow**:

- Render strings as html and not as plain text

<a name="day-15"></a>
### Day 15: June 5, 2020

**Today's Focus**: Render HTML Strings

**Progress**: 

- Content modals to render html strings properly in the body
- In process of figuring out best way to manage toggling state of all modals

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/cfe8db7b7ba081758137da53497a742f2028af31)

**Todo Tomorrow**:

- Continue management of state for modals

<a name="day-16"></a>
### Day 16: June 6, 2020

**Today's Focus**:  Modal State Management

**Progress**: 

- Got modal state management working and styled content to fit modals
- Replaced place holder images with proper brand images and optimized svgs
- Cleaned up frontend code

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/5b135cfc558d4eb63e0d5cd6c0c530e74978a9e2)

**Todo Tomorrow**:

- Add search bar and search query

<a name="day-17"></a>
### Day 17: June 7, 2020

**Today's Focus**: Add Search Bar

**Progress**: 

- Added rough search bar (still needs styling to look pretty)
- Moved fetching resources to resuable method

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/ad25e64e1f87bd4a3c802ab4bfae85972947e656)

**Todo Tomorrow**:

- Add search query

<a name="day-18"></a>
### Day 18: June 08, 2020

**Today's Focus**: Add Search Query

**Progress**: 

- Added search query, possibly need to improve db lookup performance in future
- Made search bar look prettier
- Minor refactoring to clean up code with images and brand names on frontend

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/3741e9cccc9c9bfa10461f953fc5225ede56b6a9)

**Todo Tomorrow**:

- Add categories to backend and frontend

<a name="day-19"></a>
### Day 19: June 09, 2020

**Today's Focus**: Add Categories

**Progress**: 

- Added categories and rough implementation of it on frontend
- Minor refactoring to give classes better names

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/f698c78d68edd6d9cffda788700e9a1c287a37eb)

**Todo Tomorrow**:

- Make categories pretty on frontend

<a name="day-20"></a>
### Day 20: June 13, 2020

**Today's Focus**: Filter Categories Functionality

**Progress**: 

- Filter categories on frontend

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/6f1ea0f247e5679962769957228d01eec881d566)

**Todo Tomorrow**:

- Continue working on categories on frontend

<a name="day-21"></a>
### Day 21: June 14, 2020

**Today's Focus**: Filter Categories And Search Behaviour

**Progress**: 

- Improved Search UX by adding reset search button in place of filter option when search term present
- Multiple filters can be applied to resources

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/ca7b742c98a283b110d2b2f960e3ef15624a666c)

**Todo Tomorrow**:

- write parsers for different kinds of notes

<a name="day-22"></a>
### Day 22: June 16, 2020

**Today's Focus**: Research How to Parse Resource

**Progress**: 

- Brainstormed how to parse arbitrarily formatted dates...

**Links to work**: None as just brainstorming

**Todo Tomorrow**:

- Continue brainstorm parsing dates and possibly start writing parser...

<a name="day-23"></a>
### Day 23: June 20, 2020

**Today's Focus**: Continue Research

**Progress**: 

- Continued research on how to parse resource 

**Links to work**: None as just brainstorming

**Todo Tomorrow**: 

- Implement parsing

<a name="day-24"></a>
### Day 24: June 21, 2020

**Today's Focus**: Add Date Parser 

**Progress**: 

- Added date parser to cover all formats provided by the Resources
- Added specific resource parsers to some Brands

**Links to work**: [Resources Project](https://github.com/seshieya/WooDeals/commit/6ea6a2c8622fe74ca71b07093a46889cdedea66c)

**Todo Tomorrow**:

- Refactor resource specific parsing into own services
- OR work on frontend to add an "Ends" page

<a name="day-25"></a>
### Day 25: June 26, 2020

**Today's Focus**: Algo Arrays

**Progress**: 

- Arrays & Strings - 1.1 Is Unique
- Arrays & Strings - 1.2 Check Permutation

**Links to work**: [Algo](https://github.com/seshieya/coding.questions/commit/785eb1f7e5fbd15d490b421201729a688302f4cb)

<a name="day-26"></a>
### Day 26: June 27, 2020

**Today's Focus**: Algo Arrays & Resources Add Sort by Ends Filter

**Progress**: 

- Algo
  - Arrays & Strings - 1.3 URLify
- Resources
  - Instead of adding an "Ends" page to the frontend, added and "Ends" filter to sort the resources

**Links to work**: 
- [Algo](https://github.com/seshieya/coding.questions/commit/785eb1f7e5fbd15d490b421201729a688302f4cb)
- [Resources Project](https://github.com/seshieya/WooDeals/commit/ac1df7a7ffa98fbb18d7d8a32c7996d8ddeea9d7)

**Todo Tomorrow for Resources**:

- Improve "created" and "ends" date display on the frontend
- Ensure consistent filtering is applied when filtering by categories (if end is applied first, it should be applied to categories too)

<a name="day-27"></a>
### Day 27: June 28, 2020

**Today's Focus**: Algo Arrays & Resources Show Created & Apply Consistent Sorting

**Progress**: 

- Algo
  - Arrays & Strings - 1.4 Palindrome Permutation
- Resources
  - Added created date and time to be shown on frontend
  - Sorting is consistent now when applying different category filters and when searching 
  - Toggle sorting by ends date

**Links to work**: 
- [Algo](https://github.com/seshieya/coding.questions/commit/785eb1f7e5fbd15d490b421201729a688302f4cb)
- [Resources Project](https://github.com/seshieya/WooDeals/commit/4b130ea50e05cb64ca1905138889c38efb86edce)

**Todo Next Time For Resources**:

- Write parsers for different kinds of resources
- Refactor resource specific parsing into own services

<a name="day-28"></a>
### Day 28: June 30, 2020

**Today's Focus**: Algo Arrays

**Progress**: 

- Arrays & Strings - 1.5 One Away

**Links to work**: [Algo](https://github.com/seshieya/coding.questions/commit/d42247d002262720d2033d30bc2c06965b7225de)

<a name="day-29"></a>
### Day 29: July 1, 2020

**Today's Focus**: Algo Linked Lists

**Progress**: 

- Reviewed Linked Lists
- Linked Lists - 2.1 Remove Dups

**Links to work**: [Algo](https://github.com/seshieya/coding.questions/commit/d42247d002262720d2033d30bc2c06965b7225de)

<a name="day-30"></a>
### Day 30: July 2, 2020

**Today's Focus**: Algo Linked Lists

**Progress**: 

- Linked Lists - 2.2 Return Kth To Last (in progress)

**Links to work**: None as question in progress

<!--


days missed: 18?? lost count :(

template

<a name="day-"></a>
### Day : June , 2020

**Today's Focus**: 

**Progress**: 

- 

**Links to work**: [Resources Project]()

**Todo Next Time**:

- 
- Write parsers for different kinds of resources
- Possibly improve db performance? <-- for what?? don't remember.... was it full text search for company name?
- Refactor resource specific parsing into own services
- Frontend - where sorting logic is used is really messy right now. Need to refactor to only sort when sortBy is changed, or when filtered resources is changed
- Need to further separate concerns in the components on frontend

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
