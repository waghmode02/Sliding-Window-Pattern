# Sliding-Window-Pattern :-
- A Sliding Window is used to solve problems where we need to operate on a contiguous subarray (or sublist) of a larger array (or linked list).

- It is applicable in cases where we need to
     Find longest or shortest subarray/substring meeting a particular criteria (E.g. Smallest substring with X unique characters or Longest stretch of days when stock price did not decrease). These are variable size windows.
     
  - Find a window of fixed size with contents meeting some criteria (E.g. Subarray of size N with largest sum)
  
- It involves 2 pointers. One indicating the beginning of the window and the second indicating the end.
The idea is to create a window containing a subarray and slide the window along as we traverse through the array to find the answer. 

- The window size can change by adding new elements in the end or removing elements from the beginning as we traverse.
Let's understand this with some examples.
************************************************************
#Fixed Size Window Template - Sliding Window:-

- Generally of the form: Out of all the windows of size k, find the one that satisfies the given condition.

```java
// Method to implement fixed size window algorithm
fixedSize() {
    left = 0, right = 0;   // Initialization
    while (right < n) {    // Stopping condition
        // Add right element into the window
        if (right - left + 1 == k) {   // If window size is reached
            if (condition satisfied) {
                // Update the answer
            }
            // Remove left element from the window
            left++;    // Reduce the window size
        }
        right++;    // Increase the window size
    }
}
```
#Variable Size Window Template - Sliding Window:-

- Generally of the form: Find the largest/smallest window which satisfies the given condition
```java
//To find largest window


left = 0, right = 0; //Initialization
while(right < n){
    //add right element into the window
    while(condition never going to be satisfied by increasing the window size){
        //remove left element from the window
        left++; //Reduce the window size
    }
    //update the answer
    right++; //Increase the window size
}

```
```java
//To find smallest window


left = 0, right = 0; //Initialization
while(right < n){
    //add right element into the window
    while(condition is satisfied){
       //update the answer
        //remove left element from the window
        left++; //Reduce the window size
    }
    right++; //Increase the window size
}

```
**************************************************************
#When to use this method?
- When we see a contiguous subarray problem
- When goal is to find the longest, shortest or fixed size window in the given array, string or linked list 
- When we need to reduce the Time Complexity by avoiding recalculation of values which are already in the window as we move through the array (e.g. Calculation of average of X consecutive values in an array).

#How to use this method?
- Start with a window of size 1 or a predefined size K (e.g. Subarrary of size K with the maximum sum).
- Add elements at the end and/or remove elements at the beginning of the window as we traverse along the array,  or string.



