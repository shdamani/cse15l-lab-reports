# Lab Report 5- find command
For this lab report I am going to explore a different command from the lab report 3 write up. Last time I had explored several ways to use **grep**.\
This time I am going to explore the **find** command
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
The above command finds the text file California-WhatToDO int the written_2 directory and then prompts if you want to permanently delete it.
## 3)  -exec grep 'Any text'  {} \;
This command searches for the text entered and prints the line associated with the text  and ‘-type f’ specifies the input type is a file. \
**Example 1:**
[![Screen-Shot-2023-03-12-at-4-13-07-PM.png](https://i.postimg.cc/qMfKXwgD/Screen-Shot-2023-03-12-at-4-13-07-PM.png)](https://postimg.cc/qgLgp8s2)
The above command searches for **Mumbai** in the written_2 sub-directory and prints  print lines which have Mumbai in it.\
**Example 2:**
[![Screen-Shot-2023-03-12-at-4-13-49-PM.png](https://i.postimg.cc/kMWG9mXw/Screen-Shot-2023-03-12-at-4-13-49-PM.png)](https://postimg.cc/V5LmB2tb)
The above command searches for **UCSD** in the written_2 sub-directory, but no lines are found so it prints nothing. Then it searches for **La Jolla** and prints the lines which have La Jolla in it.
## 4) -exec wc:
This command counts the number of words in the matching files
**Example 1:**
[![Screen-Shot-2023-03-12-at-4-32-12-PM.png](https://i.postimg.cc/mk6Bj8yX/Screen-Shot-2023-03-12-at-4-32-12-PM.png)](https://postimg.cc/5QvhN5GL)
The above command seraches and prints the number of words in the file Athens-Intro.txt in the written_2 sub-directory\
**Example 2:**
[![Screen-Shot-2023-03-12-at-4-34-29-PM.png](https://i.postimg.cc/KjCC4VN2/Screen-Shot-2023-03-12-at-4-34-29-PM.png)](https://postimg.cc/5QqsRsT7)
This command prints the number of words in every text file in the non-fiction sub-directory in written_2. It also prints the total words in text files of non-fiction.
