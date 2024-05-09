# Lab Report 3  

# Part 1  
1. A failure-inducing input for the buggy program method ``reversed`` in ``ArrayExamples.java`` from week 4's lab:  
   ```
   @Test
   public void testReversed2() {
     int[] input2 = { 1, 2, 3 };
     assertArrayEquals(new int[]{ 3, 2, 1 }, ArrayExamples.reversed(input2));
   }
   ```  
2. An input that doesn't induce a failure for this program:
   ```
   @Test
   public void testReversed() {
     int[] input1 = { };
     assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
   }
   ```  
3. The symptom, or the output of running the two tests above:
4. The bug, before code change required to fix it:
   ```
   static int[] reversed(int[] arr) {
      int[] newArray = new int[arr.length];
      for(int i = 0; i < arr.length; i += 1) {
         arr[i] = newArray[arr.length - i - 1];
      }
      return arr;
   }
   ```
   The bug, after code change required to fix it:
   ```
   static int[] reversed(int[] arr) {
      int[] newArray = new int[arr.length];
      for(int i = 0; i < arr.length; i += 1) {
         newArray[arr.length - i - 1] = arr[i];
      }
      return newArray;
   }
   ```
