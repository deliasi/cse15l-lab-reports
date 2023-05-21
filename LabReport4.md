# Cse 15L Lab Report 4

## Step 1: Log into ieng6
I used the command 

        ssh cs15lsp23ai@ieng6.ucsd.edu <enter> Password: <enter>
        
## Step 2: Clone your fork of the repository from your Github account
I used the command

        git clone git@github.com:deliasi/lab7  <enter>
        
        
        
## Step 3: Run the tests, demonstrating that they fail
I used the commands to run the tests

        cd lab7 <enter>
        javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>
        java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests JUnit version 4.13.2 <enter>
        
## Step 4: Edit the code file to fix the failing test
I edited the code using these commands

        vim ListExamples.java <enter>
        :set number
        :43 w i <delete> 2 
        <esc> 
        :wq
        
## Step 5: Run the tests, demonstrating that they now succeed
I used these commands to rerun the test quickly

        <up arrow> <up arrow> <up arrow> <enter>
        <up arrow> <up arrow> <up arrow> <enter>
        
## Step 6: Commit and push the resulting change to your Github account (you can pick any commit message!)
I used these commands to commit and push my changes.

        git add . <enter>
        git commit -m "Modified file" <enter>
        git push <enter>

        


  
