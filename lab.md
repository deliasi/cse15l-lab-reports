# Lab Report 1 CSE 15L
Hello class, today I will give a step by step tutorial on how to log into a course-specific account on ieng6.

## Step 1: installing VScode
I already had VS code downloaded on my computer, but the first step must be to access Visual Studio Code on your personal app store or website.
 <br>Download [Visual Studio](https://code.visualstudio.com/) and follow instructions to install.
 <li>Once VS code is open, this is what should be shown. 


 <img src = "https://user-images.githubusercontent.com/130005419/230982176-812e9336-bd10-46de-bac3-9f8bc1ee4eeb.png">
 </li>
      
<li> To remotely access your account, go to terminal in Visual Stuido code. This is done by clicking on the "Go to termianl bar", then clicking "new terminal". 
 </li>
 

## Step 2:  Remotely Connecting
 <br>Download [Visual Studio](https://code.visualstudio.com/) and follow instructions to install.
<br>Find your specific account at [SDacs Ucsd](https://sdacs.ucsd.edu/~icc/index.php). 
<li>Once prompted, set new password for your course specific account. Go to the termianl in VS Code and type 
 
        $ ssh cs15lsp23zz@ieng6.ucsd.edu
However, replace the "zz" in the message with letters from your course-specific account.
<li> Enter yes after asked if you want to continue logging in and ensure authenticity! Then, you will be asked to enter your password in order to connect to the your account. 
<li> Once you enter your password and connect, you should see something like this.
 </li>
 <img src = "https://user-images.githubusercontent.com/130005419/230987541-7d3b3faa-1c18-4dc1-b7b0-0b1fd59b0bcb.png">

<br>
## Step 3: Trying Some Commands
<ol>
 
<li> In the terminal, try various commands to get familiar with them all. 
 <li> One example command I tried and found useful was 
         
          cat /home/linux/ieng6/cs15lsp23/public/hello.txt.
 Calling the cat command would read the file parameter and display the standard output.
 
<img src = "https://github.com/deliasi/cse15l-lab-reports/blob/main/Screen%20Shot%202023-04-23%20at%203.41.35%20PM.png">
   </li>
  <br>
  <li> Another useful command to try would be 
   
           ls -lat
   The ls command is key for listing the conetnst of the specific working directory you want.
   
<img src = "https://github.com/deliasi/cse15l-lab-reports/blob/main/Screen%20Shot%202023-04-23%20at%203.39.40%20PM.png">
   <br>
   <li> Another example of a command I tried and think would be useful to practice with would be 
    
            cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/
   Using the cp command will not always produce a direct output as seen below, but is useful for copying the contents of a file into a more specifieced source file.
    
 <img src = "https://github.com/deliasi/cse15l-lab-reports/blob/main/Screen%20Shot%202023-04-23%20at%203.49.28%20PM.png">
   <br>
    
<li> Some more example commands are: cd, ls -a, ls <directory> (where directory is replaced by an actual specific directory>, ls -lat, cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/, cat /home/linux/ieng6/cs15lsp23/public/hello.txt
<li> Certain commands have differents uses, but all commands are useful.
 <br> I recommend using the commands with different parameters in order to notice the change in output. 
 <br> Understanding the purpose of each command allows for a far more broad use amongst multiple files.
 <br> Being able to use these commands succesfully will allow you to list contents of working directories, move between directories, and ultimately give you power to alter the contents of your files.
<li> If all is correct, you should see something like this when commands are run!

<img src = "https://user-images.githubusercontent.com/130005419/230987757-621998fd-b815-4d8d-8044-9dd47457bceb.png">

<li> Your results may look different based on the commands you choose, but I recommend trying ls -lat, ls -a, and cd to begin.

 
