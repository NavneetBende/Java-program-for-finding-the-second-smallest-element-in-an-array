# Java-program-for-finding-the-second-smallest-element-in-an-array

Second Smallest Element in an array in Java
Here, in this page we will discuss the program to find the second smallest element in an array using java programming language. We are given with an array and need to print the second smallest element among them.

Second smallest element in an array in java
Various Method Discuss in this page are :
Method 1 : Using two loops
Method 2 : Using one loop
 

Method 1 :
Take a variable say smallest = Integer.MAX_VALUE
Run a loop over the entire array and check if (arr[i]<smallest)
Then set smallest = arr[i].
Declare another variable say sec_smallest = Integer.MAX_VALUE
Run a loop and check if arr[i] != smallest and arr[i] < sec_smallest
Then print(sec_smallest) after completing the iteration.
Second smallest element java
Method 1 : Code in Java
Run
import java.util.Scanner;
import java.util.*;

public class Main
{ 
   static int secSmallest(int arr[], int n)
   {
      // assigning first element as smallest temporarily
      int smallest = arr[0];

      // we find the smallest element here
      for (int i=0; i < n; i++){
         if(arr[i] < smallest)
            smallest = arr[i];
      }

     // temporarily assinging largest max value
     int sec_smallest = Integer.MAX_VALUE;


     // finding second smallest here
     for (int i=0; i < n; i++){
         if(arr[i] != smallest && arr[i] < sec_smallest)
           sec_smallest = arr[i];
     }

    return sec_smallest;

  }
  public static void main(String args[])
  {

      int arr[] = {12, 13, 1, 10, 34, 10};
      int n = arr.length;
      System.out.print(secSmallest(arr, n)); 
   }
}
Output :
10
Related Pages
Find Smallest Element in an Array
 
Find the Smallest and largest element in an array

Calculate the sum of elements in an array 

Reverse an Array

Sort first half in ascending order and second half in descending 

Method 2 :
Declare two variables say first = INT_MAX and second = INT_MAX to hold the first and second smallest elements respectively.
Now, iterate over the entire array i.e, from index 0 to n-1
Inside the loop check if (arr[i]<first) then set second = first and first = arr[i].
Else check if(second > arr[i]) then set second = arr[i]
After complete iteration print the value of second.
Method 2 Code in Java
Run
import java.util.Scanner;
import java.util.*;

public class Main
{ 
   static int secSmallest(int arr[], int n)
   {
        int first = Integer.MAX_VALUE, second = Integer.MAX_VALUE;

        for (int i=0; i < n; i++){
            if(arr[i] < first){ second = first; first = arr[i]; } else if(second>arr[i])
           second = arr[i];
        }

        return second;

   }
   public static void main(String args[])
   {

      int arr[] = {12, 13, 1, 10, 34, 10};
      int n = arr.length;
      System.out.print(secSmallest(arr, n)); 
   }
}
Output :
10
