# Lab Report 5
For this lab report I am going to explore a different command from the lab report 3 write up. Last time I had explored several ways to use **grep**.\
This time I am going to explore the find command
## 1) -name 
This command searches a file with specific name.\
**Example 1:**
[![Screen-Shot-2023-03-12-at-3-48-43-PM.png](https://i.postimg.cc/pLxSmDH3/Screen-Shot-2023-03-12-at-3-48-43-PM.png)](https://postimg.cc/F7Wpqk1x)
The above command searches where the text file WhereToIndia is located in the written_2 directory and returns its path from there.\
**Example 2:**
[![Screen-Shot-2023-03-12-at-3-58-35-PM.png](https://i.postimg.cc/28J6mSNq/Screen-Shot-2023-03-12-at-3-58-35-PM.png)](https://postimg.cc/GHFrxr2r)
The above command searches where the text file California-WhatToDO is located in the travel_guides directory and returns its path from there.
## 2)  -exec rm -i {} \; 
This command finds and deletes a file with confirmation.\
**Example 1:**
[![Screen-Shot-2023-03-12-at-4-05-55-PM.png](https://i.postimg.cc/tCg5w29q/Screen-Shot-2023-03-12-at-4-05-55-PM.png)](https://postimg.cc/NLWmr8yS)
The above command finds the text file WhereToIndia int the travel_guides sub-directory and then prompts if you want to permanently delete it.\
**Example 2:**
[![Screen-Shot-2023-03-12-at-4-07-56-PM.png](https://i.postimg.cc/8CgLpHgr/Screen-Shot-2023-03-12-at-4-07-56-PM.png)](https://postimg.cc/FYGYG0R9)
The above command finds the text file California-WhatToDO int the written_2 directory and then prompts if you want to permanently delete it.\
## 3)  -type f -name "*.txt" -exec grep 'Any text'  {} \;

**Example 1:**
[![Screen-Shot-2023-03-12-at-4-13-07-PM.png](https://i.postimg.cc/qMfKXwgD/Screen-Shot-2023-03-12-at-4-13-07-PM.png)](https://postimg.cc/qgLgp8s2)\
