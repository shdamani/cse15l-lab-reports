# LAB REPORT 2 - SHLOK DAMANI A17373189 #
## In the following I will ##
- Write a web server called StringServer
- Analyze a bug from the week 3 lab session and fix it
- What I learned in the last 2 weeks :)
## 1) Web server ##

[![Screen-Shot-2023-01-28-at-12-10-44-PM.png](https://i.postimg.cc/qBsvBLws/Screen-Shot-2023-01-28-at-12-10-44-PM.png)](https://postimg.cc/SjKhDcwR)
\
[![Screen-Shot-2023-01-28-at-12-14-01-PM.png](https://i.postimg.cc/7LxTY4sf/Screen-Shot-2023-01-28-at-12-14-01-PM.png)](https://postimg.cc/fVrbBGhN)
\
```java
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String s="";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format(s);
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")){
                for(int i=1;i<parameters.length;i++){
                   s=s+parameters[i];
                }
                String s1=s;
                s=s+"\n";
                return String.format(s1);
            }
            }
            return "404 Not Found!";
        }
    }
}
```
```java

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

In both of the screenshots, first, the handleRequest and main method is called. The argument to call the main method is  port 4078 and the argument to call handleRequest is the URL. Everytime a new message is added through the url address or when the survey is run the value of **s** is appended and a new line is added. The new message is added to the original empty String s where path[1] is the new message added, and it also moves to the next line everytime.

## 2) Analyzing the bug ##
**A failure-inducing input for the buggy program**
 ```
@Test
  public void testReversed2() {
    int[] input1 = {1,2,3};
    assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input1));
  }
  ```
The problem with this method is that the new value of input1 is [0,0,0]} as the assignment is reversed. hence the method returns [0,0,0] and the test fails \
**An input that doesn’t induce a failure**
 ```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
 ```
In the above test the length of the array is zero so it would enter the for loop, hence the orignal empty int array will be returned and the test would pass\
**The symptom, as the output of running the tests**
[![Screen-Shot-2023-01-28-at-5-58-54-PM.png](https://i.postimg.cc/ZntW2vQv/Screen-Shot-2023-01-28-at-5-58-54-PM.png)](https://postimg.cc/mzjZFkBT)
**The bug I have chosen is from the method:**
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
**The code after fixing it**
Reversing the assignment \n
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
       newArray[arr.length - i - 1]=arr[i];
    }
    return arr;
  }
```
In the above code the elements of a the newArray were being assigned to arr in reverse order, hence arr becomes an array of all 0 values. The bug can be fixed by switching the assignment.

## What did I learn from week 1 and week 2 ##
Making your own webpage for the first time. What are symptoms and bugs in a program. And mainly I learnt about junit testing, which is very cse 12 programming assignments.
