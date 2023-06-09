# Lab Report 2 CSE 15L

## Part: StringServers
I began by creating the contents of my StingerServer program.  

 <img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-04-23%20at%207.54.12%20PM.png">
    

Then, I tested my code by searching on the web with the local host and port number, followed by the message I wanted to add. The message I wanted to display first was my name, derrick.
 
  <img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-04-19%20at%204.39.20%20PM.png">
    

  The method which is called is
          
	  handleRequest

  <li>One of the relevant arguments within the method is url.getpath and contains. This is what ultimately matches our string url in order to display the correct output.
	</li>
  <li>Another important argument is the String array called parameters which splits the url so that the first half is equal to the second.
	</li>
  <li>Another important argument is equalling the parameter array index at 0 with our desired outcome. 
	</li>
  <li>Through our code, the value of our url is added to and consistently compared to make sure we stay on the right track. In our method, url is split in order to compare its two halves.
   </li>
   
   The next message I wanted to print was, "Hiii".
  
 <img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-04-19%20at%204.39.20%20PM.png">
   
   The method which is called is 
   
             public static void main(String[] args) throws IOException
	
  
   The main method in StringServer class is called, which takes in String array args[] and of port number. 
   We compare our argument length to make sure that it is a valid number. The values of our String s and Url are changed due to the new commands being displayed.
   <li>The specific value of my relevant field was 4000, which stood as my port number. This value is apart of my relevant field. The 
   port number does not change bacsue it is used to access the local host.
	</li>
   <li>Through out handler method, our url is split in two and both sides of our url are set equal to one another. Our String s contents if changed by the contents of url. As the code runs, more is added to our url, which ultimately is returned into our String s.
	</li>
 
  
## Part 2: Bugs
<br>In order to cause failure from the written code, I used the tests below.
  
          @Test
          public void testReversedInPlace2() {
            int[] input1 = {2,3,4};
            assertArrayEquals(new int[]{4,3,2}, ArrayExamples.reversedInPlace(input1));
         }
         
         
          @Test
          public void testReversed2() {
            int[] input1 = {2,3,4};
            assertArrayEquals(new int[]{4,3,2}, ArrayExamples.reversed(input1));
         }
	 
   <br>
   Inputs to the same written code that did not cause failure are shown below.
   
           @Test 
	   public void testReverseInPlace() {
              int[] input1 = { 3 };
              ArrayExamples.reverseInPlace(input1);
              assertArrayEquals(new int[]{ 3 }, input1);
	         }


          @Test
          public void testReversed() {
             int[] input1 = { };
             assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
          }
          
   <br>
   
   The sympton, as the output of running these tests is shown below.
   <img src = "https://raw.githubusercontent.com/deliasi/cse15l-lab-reports/main/Screen%20Shot%202023-04-24%20at%204.57.14%20PM.png">
      <br>

   In order to pass all the tests, we had to fix the buggy code.
   Before the code was fixed it looked as so.
   
           static void reverseInPlace(int[] arr) {
               for(int i = 0; i < arr.length; i += 1) {
                  arr[i] = arr[arr.length - i - 1];
           }
       }
       
           static int[] reversed(int[] arr) {
              int[] newArray = new int[arr.length];
             for(int i = 0; i < arr.length; i += 1) {
                arr[i] = newArray[arr.length - i - 1];
           }
          return arr;
       }
<br>

  Once I changed the contents of my code, it looked as so.
  
          static void reverseInPlace(int[] arr) {
               if (arr == null || arr.length <= 1) {
                   return;
           }
 
          int len = arr.length;
          for (int i = 0; i < len / 2; i++) {
              int tempFront = arr[i];
              int tempLast = arr[len - i - 1);
              arr[i] = tempLast;
              arr[len - i -1] = tempFront;
           }
       }
       
       
           static int[] reversed(int[] arr) {
              int[] newArray = new int[arr.length];
              for(int i = 0; i < arr.length; i += 1) {
                  newArray[arr.length - i - 1] = arr[i];
           }
          return newArray;
       }
       
 <br>
 
 For the method
 
         reverseInPlace()
	
 The code was buggy because it was setting our old array equal to the desired new one without keeping track of our initial array value. I needed to create new temp values to switch the array elements, until it reached the middle element; Then, I needed to set my new array to that temp value as so.
 
 For the 
 
         reversed() 
	 
 method, the code was modifying the old array, and it didn’t even return the new one! The arr[i] was being modified in the original for loop. So I need to reassign the value and make sure the correct array is being returned. 
  
 
## Part 3: Something I Learned
 <li> Throughout the process of fixing the buggy code in lab 3, I learned that taking advantage of JUnit tests is essential in ensurring that you have the correct contents. As we saw, there is always the possibility that certain tests can still pass faulty code, however, by creating various different tests, I was more able to recognize the mistake within the code. I did not grasp the advantage of creating these tests until I had to deal with incorrect methods given to me.

