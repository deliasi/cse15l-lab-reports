# CSE 15L Lab Report 5
## Part 1: Debugging Scenario 

## Issue: DocSearchServer not Running Accordingly

**Environment**: Macbook Air 2015; Mac OS; Chrome; VS Code

**Context**: As I try to run my DocSearcgServer, the code results in and index out of bounds order. Am i possibly using an incorrect command?

<img width="760" alt="Screenshot 2023-05-31 at 19 30 45" src="https://github.com/rcwoshimao/cse15l-lab-reports/assets/108894739/89771c8c-88ef-4645-88b7-64650ba521cf">
<br>

**Symptom**: I expected to get a server and local server running.

```console
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 1 out of bounds for length 1
        at DocSearchServer.main(DocSearchServer.java:75)
```

## Response with leading question
TA: 
Thanks for your question Derrick, it seems that you compiled your files correctly but did not include certin commands needed after your port number. I recommentlooking over your class and add what is needed. 

## Student Fix:
Wow, that helps me a lot, I noticed that I did not include a path for my server. I chose to add technical/government after mt port number in order to fix my code.

<img width="762" alt="Screenshot 2023-05-31 at 19 31 52" src="https://github.com/rcwoshimao/cse15l-lab-reports/assets/108894739/50d00e22-46f2-41fd-b9d3-3d3a2f81b83b">
<br>
<img width="664" alt="Screenshot 2023-05-31 at 19 11 59" src="https://github.com/rcwoshimao/cse15l-lab-reports/assets/108894739/95548c22-1679-4b27-bfc3-7bf9fb879bb1">
<br>
<img width="738" alt="Screenshot 2023-05-31 at 19 12 08" src="https://github.com/rcwoshimao/cse15l-lab-reports/assets/108894739/d7b74dfc-1ce0-42ce-8500-f213701236f8">
<br>

### All the info needed about the set up
[DocSearch repository](https://github.com/rcwoshimao/docsearch). 
Contents of each file before fixing the bug:  
    - lib/
    - technical/
    - DocSearchServer.java
    - README.md
    - Server.java
    - TestDocSearch.java
    - docsearch.sh

Command that triggers the bug: 

```console
DERRICKS-MacBook-Air:docsearch-main alenooshhambarchian$ ~ % cd desktop/docsearch-main 
DERRICKS-MacBook-Air:docsearch-main alenooshhambarchian$ docsearch-main % javac DocSearchServer.java Server.java 
DERRICKS-MacBook-Air:docsearch-main alenooshhambarchian$ % java DocSearchServer 3000
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 1 out of bounds for length 1
        at DocSearchServer.main(DocSearchServer.java:75)    `
```

## Part 2: Reflection
The most memorable thing I learned in the second quarter was the use of commands such as grep. The grep command makes it so much simpler to find the details of text. By using the grep command, I can access the details of any text I want and find information about such text. It makes coding much more interesting and added a new use to the terminal.

