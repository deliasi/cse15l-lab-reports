# Lab Report 2 CSE 15L

## Part 1: StringServers
I began by creating the contents of my StingerServer program.  

 <img src = "https://user-images.githubusercontent.com/130005419/230982176-812e9336-bd10-46de-bac3-9f8bc1ee4eeb.png">
 
 Then, I tested my code by searching on the web with the local host and port number, followed by the message I wanted to add.
 
  <img src = "https://user-images.githubusercontent.com/130005419/230982176-812e9336-bd10-46de-bac3-9f8bc1ee4eeb.png">
  
  <li>The handleRequest method is called
  <li>One of the relevant arguments within the method is url.getpath and contains. This is what ultimately matches our string url in order to display the correct
  output.
  <li>Another important argument is the String array called parameters which splits the url so that the first half is equal to the second.
  <li>Another important argument is equalling the parameter array index at 0 with our desired outcome. 
  <li>Through our code, the value of our url is added to and consistently compared to make sure we stay on the right track. In our method, url is split in order to compare its two halves.
  
 <img src = "https://user-images.githubusercontent.com/130005419/230982176-812e9336-bd10-46de-bac3-9f8bc1ee4eeb.png">
   
   The StringServer method is called and is very important.
   In order to check if we have a valid port number, through this method, we compare our argument length to ensure we are on the right track.
   The specific value of my relevant field was 4000, whcih stood as my port number. This value is apart of my relevant field. The 
   port number does not change bacsue it is used to access the local host.
   Through out handler method, our url is split in two and both sides of our url are set equal to one another. Our String s
