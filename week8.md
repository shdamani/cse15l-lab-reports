# Lab Report 4 #
## Challenge Tasks ##
1. Deleting any existing forks of the repository \
[![Screen-Shot-2023-02-26-at-3-54-58-PM.png](https://i.postimg.cc/QxjvbdK1/Screen-Shot-2023-02-26-at-3-54-58-PM.png)](https://postimg.cc/QVn6Nsbd)

2. Forking the repository \
[![Screen-Shot-2023-02-26-at-3-58-48-PM.png](https://i.postimg.cc/66zg3NT0/Screen-Shot-2023-02-26-at-3-58-48-PM.png)](https://postimg.cc/23b2cMQb)

3. Logging into ieng6 \
Keys pressed: <kbd>ENTER<kbd>\
For this step I typed **ssh cs15lwi23aex@ieng6.ucsd.edu** to log into my student specific ieng6 account. Password wasnt required for my personal device as 
ssh keys were generated during the last lab session.
[![Screen-Shot-2023-02-26-at-4-02-31-PM.png](https://i.postimg.cc/W3mNhnxp/Screen-Shot-2023-02-26-at-4-02-31-PM.png)](https://postimg.cc/WF3LyM2x)

4. Cloning the Repository \
Keys pressed:<kbd>CMD+C<kbd> + <kbd>CMD+V<kbd> + <kbd>ENTER<kbd>
For this step I first copied the ssh url of the above forked repository then typed **git clone** then pasted the url from the clipboard.
[![Screen-Shot-2023-02-26-at-4-07-21-PM.png](https://i.postimg.cc/BbdMkTQD/Screen-Shot-2023-02-26-at-4-07-21-PM.png)](https://postimg.cc/7Jn3TTzY)

5. Running the Junit Tests \
a)Keys pressed: <ENTER> \
  cd lab7 \
b)Keys pressed: <CMD+C><CMD+V><ENTER> \
  The __javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java__ was copied on the clipboard and pasted on the terminal to compile the 2 files in the directory. \
c)Keys pressed: <CMD+C><CMD+V><ENTER> \
  the __java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests__ was copied on the clipboard and pasted on the terminal to compile the 2 files in the directory. \
[![Screen-Shot-2023-02-26-at-4-18-33-PM.png](https://i.postimg.cc/brNZPWdf/Screen-Shot-2023-02-26-at-4-18-33-PM.png)](https://postimg.cc/WFCN69M5)

6.Edit the code file to fix the failing test \
Keys Pressed: <ENTER>, <SCROLLING Till lne 43><backspace><2>, <CTRL+O><CTRL+X><n> \
The code can be edited using nano. The error was found at the line 43 where after pressing the right 13 times index1 was changed to index2 and the changes were saved and I exited from nano.
[![Screen-Shot-2023-02-26-at-4-29-26-PM.png](https://i.postimg.cc/Hx7gytK8/Screen-Shot-2023-02-26-at-4-29-26-PM.png)](https://postimg.cc/8JD98LTT)
