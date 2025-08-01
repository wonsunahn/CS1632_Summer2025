TEST FIXTURE:
1. Firefox browser version >= 105, or Chrome browser version >= 105 is installed and launched.

TEST CASES:

```
IDENTIFIER: TEST-1-TITLE
TEST CASE: Check that title of the home page is "Home | University of Pittsburgh".
PRECONDITIONS: None.
EXECUTION STEPS: None.
1. Open the URL https://www.pitt.edu/ on the web browser.
POSTCONDITIONS:
* The title of the page is "Home | University of Pittsburgh".
  (Use "assert title" command.)
```

```
IDENTIFIER: TEST-2-LOGO-EXISTS
TEST CASE: Check that the logo with alt text "University of Pittsburgh" exists.
PRECONDITIONS: None.
EXECUTION STEPS:
1. Open the URL https://www.pitt.edu/ on the web browser.
POSTCONDITIONS: 
* A logo with the alt text "University of Pittsburgh" is present on the page.
  (Use "assert element present" command on locator with "University of Pittsburgh" as alt text.)
```

```
IDENTIFIER: TEST-3-LOGO-IMAGE
TEST CASE: Check that the "University of Pittsburgh" logo uses image "/sites/default/files/assets/pitt_shield_white-home.png"
PRECONDITIONS: None.
EXECUTION STEPS:
1. Open the URL https://www.pitt.edu/ on the web browser.
POSTCONDITIONS: 
* The "University of Pittsburgh" logo img has an src attribute with value "/sites/default/files/assets/pitt_shield_white-home.png".
  (Use "store attribute" command followed by "assert" command.)
```

```
IDENTIFIER: TEST-4-SCHOOLS-SCI
TEST CASE: Check that the 3rd item in the school list is "Computing & Information".
PRECONDITIONS: None.
EXECUTION STEPS:
1. Open the URL https://www.pitt.edu/ on the web browser.
2. Click on the "hamburger" icon (three horizontal lines).
POSTCONDITIONS: 
* The 3rd li element in the schools list is "Computing & Information".
  (Use "assert text" command on xpath that contains li[3].)
```

```
IDENTIFIER: TEST-5-SCHOOLS-COUNT
TEST CASE: Check that there are 15 areas in the research areas page.
PRECONDITIONS: None.
EXECUTION STEPS:
1. Open the URL https://www.pitt.edu/ on the web browser.
2. Click on the "hamburger" icon (three horizontal lines).
POSTCONDITIONS: 
* There are exactly 16 li elements in the schools list.
  (Use "assert element present" for li[16] followed by "assert element not present" for li[17].)
```

```
IDENTIFIER: TEST-6-SEARCH-CSC
TEST CASE: Check that the third item when searching "csc" is the CSC Officers page.
PRECONDITIONS: None.
EXECUTION STEPS:
1. Open the URL https://www.pitt.edu/ on the web browser.
2. Click on the search icon.
3. Type "computer science club" in the search box that pops up.
4. Click on the "SEARCH" button.
POSTCONDITIONS: 
* Somewhere in the search results is the item:
  "Student Organization Spotlight: Computer Science Club (CSC)".
  (Use "assert element present" command on locator with the above as the element text.)
```
