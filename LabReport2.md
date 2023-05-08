# Lab Report 2 CSE 15L

## Part 1: StringServers
I already had VS code downloaded on my computer, but the first step must be to access Visual Studio Code on your personal app store or website.
 <br>Download [Visual Studio](https://code.visualstudio.com/) and follow instructions to install.
 <li>Once VS code is open, this is what should be shown. 


 <img src = "https://user-images.githubusercontent.com/130005419/230982176-812e9336-bd10-46de-bac3-9f8bc1ee4eeb.png">
 </li>
      
<li> To remotely access your account, go to terminal in Visual Stuido code. This is done by clicking on the "Go to termianl bar", then clicking "new terminal". 
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
	
 I needed to create new temp values to switch the array elements, until it reached the middle element;
 
 For the 
 
         reversed() 
	 
 method, the code was modifying the old array, and it didn’t even return the new one! So I need to reassign the value and make sure the correct array is  being returned. 
  
 </li>
 
 </br>
 
 ## Part 3: Something I Learned
 <li> Throughout the process of fixing the buggy code in lab 3, I learned that taking advantage of JUnit tests is essential in ensurring that you have the correct contents. As we saw, there is always the possibility that certain tests can still pass faulty code, however, by creating various different tests, I was more able to recognize the mistake within the code. I did not grasp the advantage of creating these tests until I had to deal with incorrect methods given to me.

