# Cse 15L Lab Report 4

## Step 1: Log into ieng6
I used the command 

        ssh cs15lsp23ai@ieng6.ucsd.edu <enter> Password: <enter>

<li> Using these commands, I was able to enter my ieng6 account quicker, without the need of using a password. Pressing
        enter directly logged me into my account.
<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-05-20%20at%209.46.54%20PM.png">
</li>  

## Step 2: Clone your fork of the repository from your Github account
I used the command

        git clone git@github.com:deliasi/lab7 <enter>
        

<li> A quick way to clone my fork respitory into my github was by generating ssh keys. This way, I was able to 
        use the command above and then press enter to clone.        
<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-05-20%20at%2010.25.09%20PM.png">
</li>   

## Step 3: Run the tests, demonstrating that they fail
I used the commands to run the tests

        cd lab7 <enter>
        javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>
        java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
        JUnit version 4.13.2 <enter>
        
<li> I first used cd to enter into my lab7 directory. Then I used javac and java commands to run my ListExamplesTests file.        
<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-05-20%20at%2010.29.21%20PM.png">
 </li>   

## Step 4: Edit the code file to fix the failing test
I edited the code using these commands

        vim List <tab> .java <enter>
        :set number
        :43 w i <delete> 2 
        <esc> 
        :wq
                
<li> I accessed my code using 
        
        vim List <tab>
       
(tab allowed Examples to be displayed without me having to type it) and then 
        
        .java <enter>
which got me into  the code.
 </li>       

<li> Once I was in my code, I accessed the line of code I wanted to change, and made the changes needed above.
 The commands
        
     w i
        
 helped me move through my code quicker and insert values.
  </li> 
         
                
<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-05-20%20at%2010.41.17%20PM.png">
        </li>
        </li>

## Step 5: Run the tests, demonstrating that they now succeed
I used these commands to rerun the test quickly

        <up arrow> <up arrow> <up arrow> <enter>

        <up arrow> <up arrow> <up arrow> <enter>
<li>  Using up arrows was a good way to rerun my tests quickly without having to type out the 
                        
     javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>
     java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
        
commands. Those commands were three up in history when I needed to access them, so I used the appropriate number of up keys.
                        
 <img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-05-20%20at%2010.42.05%20PM.png">
        </li>   
        

## Step 6: Commit and push the resulting change to your Github account (you can pick any commit message!)
I used these commands to commit and push my changes.

        git add . <enter>
        git commit -m "Modified file" <enter>
        git push <enter>
        
<li> I first added my changes to the file. Then, I committed the changes creating a new
        modified file. Finally, I pushed these changes to my github respiratory.    
<img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-05-20%20at%2010.56.51%20PM.png">


  
