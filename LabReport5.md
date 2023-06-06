# CSE 15L Lab Report 5
## Part 1: Debugging Scenario 

## DocSearchServer not Running Accordingly

Ran on Macbook Air 2015 Mac OS Chrome VS Code

As I try to run my DocSearchServer, the code results in and index out of bounds order. Am i possibly using an incorrect command?

<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-06-05%20at%204.34.26%20PM.png">
<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-06-05%20at%204.34.32%20PM.png">

<br>

I expected to get a server and local server running.

```console
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 1 out of bounds for length 1
        at DocSearchServer.main(DocSearchServer.java:75)
```

## Response
TA: 
Thanks for your question Derrick, it seems that you compiled your files correctly but did not include certain commands needed after your port number. I recommend looking over your class and add what is needed. 

## Student Fix:
Wow, that helps me a lot, I noticed that I did not include a path for my server. I chose to add technical/government after my port number in order to fix my code.

<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-06-05%20at%205.15.09%20PM.png">
<br>
<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-06-05%20at%204.37.38%20PM.png">
<br>
<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-06-05%20at%204.38.13%20PM.png">
<br>

### Set Up
[DocSearch repository](https://github.com/rcwoshimao/docsearch). 
Contents of each file before fixing the bug:  
    - Server.java
    - TestDocSearch.java
    - docsearch.sh
    - lib/
    - technical/
    - DocSearchServer.java
    - README.md
    
Command that triggers the bug: 

```console
DERRICKS-MacBook-Air:~ alenooshhambarchian$ cd desktop/docsearch-main
DERRICKS-MacBook-Air:docsearch-main alenooshhambarchian$ javac DocSearchServer.java Server.java 
DERRICKS-MacBook-Air:docsearch-main alenooshhambarchian$ java DocSearchServer 3000
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 1 out of bounds for length 1
        at DocSearchServer.main(DocSearchServer.java:75)    `
```

## Part 2: Reflection
The most memorable thing I learned in the second quarter was the use of commands such as grep. The grep command makes it so much simpler to find the details of text. By using the grep command, I can access the details of any text I want and find information about such text. It makes coding much more interesting and added a new use to the terminal.

