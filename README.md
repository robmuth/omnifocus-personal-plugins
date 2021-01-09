# My Personal OmniFocus 3 Plug-Ins

## Sort Projects
I have a long projects list and want it alphabetical sorted, but specified projects should always be at the top and others at the bottom.
That is, *Orga Allgemein* remains at the top, as well as *Memo* and *Templates* always at the bottom.
However, the folder *TU* should always be the second entry.
The script sorts projects and folders the same, including all sub-folders.

You can specify the positions with relative order:
```javascript
const positions = [
    { "order": 0,  "name": "Orga Allgemein" }, 
    { "order": 0,  "name": "TU Orga Allgemein" },
    { "order": 1,  "name": "TU" },
    { "order": -1, "name": "Memo" },
    { "order": -1, "name": "Templates" }
];
```

## Sort Reading List
I have an automatically organized reading list for papers and links.
Therefore, I save the title and URL as new task and assign specified keywords.
The plug-in then moves the URL to the note (so they become click-able) and sorts them into categories by their keywords.
The categeories are expandable tasks (if it does not exists it will be created automatically).

There are three special kewords:
- *ASAP* sets its due date to today
- *Read* adds current date and moves it to read category
- *Inbox* for tasks which could not be sorted (no assigned keyword?)

You can specify the categories and their order:
```javascript
const categories = ["Read", "Paper", "Novel", "Tool", "Misc", "ASAP", "Fun", "Explore", "Voting", "Promotion", "Skills", "Inbox"];
```
