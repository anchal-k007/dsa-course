# DSA Course
This repo contains all the questions which I found important in the striver DSA course [link](https://takeuforward.org/strivers-a2z-dsa-course/strivers-a2z-dsa-course-sheet-2)

---

The structure of the repo is as follows
1. An appendix section contains some useful links for certain concepts
2. A H2 heading will contain the broad topic, for example - Arrays, Trees, Graphs, etc.
3. Each topic will have sub-headings. Each sub-heading will mean a different level for the question of that topic.
4. There will be a list of questions of each category level. It will contain the different links for that question, including videos, questions, articles, different solutions, etc.

## Appendix
Links of important concepts 
* **C++ STL Basics**
  * [Striver](https://www.youtube.com/watch?v=RRVYpIET_RU)
  * [Luv Babbar](https://www.youtube.com/watch?v=WgMPrLX-zsA)
    
* **Custom Sorting Function** : If you want to swap, return `false`
  * [Luv](https://www.youtube.com/watch?v=3pvZhwp0U9w)
  * Most common method is to return the actual order you want. For example to sort an array in decreasing order `return num1 > num2;`
    
* **Custom Sorting Comparator In Priority Queue** : If you want to swap, return `true` 
  * [GFG](https://www.geeksforgeeks.org/custom-comparator-in-priority_queue-in-cpp-stl/)
  * When `true` is returned, it means the order is correct and **NO swapping** of elements takes place.
  * Return the reverse order of which you want at the top of your priority queue
  * ```cpp
    class Compare {
        public:
           bool operator()(T a, T b){
               if(cond){
                   return true;
               }
               return false;
          }
    };
    ```
    
* **Lambda Functions** : Basic syntax
  ```cpp
  [ capture clause ] (parameters) -> return-type  
  {   
     definition of method   
  } 
  ```
  * Can ignore capture clause and return-type in most cases
  * Most common usage (sorts the vector in given order)
    ```cpp
    sort(a.begin(), a.end(), [](int a, int b) -> {
    		return a > b;
    }
    ```
  * [GFG Article](https://www.geeksforgeeks.org/lambda-expression-in-c/)
     
---

Template

 * Question Name:
   * Description 
   * [LeetCode]()  
   * [Striver Article]()  
   * [GFG]()  

---

## Arrays

### Easy

  * **Kadane's Algo**: **Very Important**
    * Used to find the maximum possible sum present in a subarray
    * [LeetCode](https://leetcode.com/problems/maximum-subarray/description/)
    * [Striver Article](https://takeuforward.org/data-structure/kadanes-algorithm-maximum-subarray-sum-in-an-array/)  

 * Union of 2 Sorted Arrays:
   * Handling duplicates is the catch
   * [Striver Article](https://takeuforward.org/data-structure/union-of-two-sorted-arrays/)  
   * [GFG](https://www.geeksforgeeks.org/problems/union-of-two-sorted-arrays-1587115621/1)  

### Medium

  * Rotate Array K times:
    * There are many approaches, the most optimal is medium level, especially finding out the edge case. If not found, then it won't be solvable 
    * [LeetCode](https://leetcode.com/problems/rotate-array/description/)
    * [Striver Article](https://takeuforward.org/data-structure/rotate-array-by-k-elements/)
      
  * Next permutation: A nice, interesting question
    * [LeetCode](https://leetcode.com/problems/next-permutation/description/)
    * [Striver Article](https://takeuforward.org/data-structure/next_permutation-find-next-lexicographically-greater-permutation/)
      
  * Stock Buy and Sell: There are a lot of iterations of this problem, which is essentially a set of DP problems. But the first iteration of the problem can be solved by simply using arrays
    * [LeetCode](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)  
    * [Striver Article](https://takeuforward.org/data-structure/stock-buy-and-sell/)

 * **Subarray with Sum K**: **Important**
   * Using a map to store prefix sum values is an important concept. This is used in many questions. Have encountered it in OAs as well
   * [Striver Article](https://takeuforward.org/arrays/longest-subarray-with-sum-k-postives-and-negatives/) [Striver Article 2](https://takeuforward.org/arrays/count-subarray-sum-equals-k/)  
   * [GFG](https://www.geeksforgeeks.org/problems/longest-sub-array-with-sum-k0809/1)
   * [LeetCode](https://takeuforward.org/arrays/count-subarray-sum-equals-k/)

 * **Merge Intervals**: **Important**
   * This question forms the basis of a lot of DP problems
   * [Striver Article](https://takeuforward.org/data-structure/merge-overlapping-sub-intervals/)  
   * [LeetCode](https://leetcode.com/problems/merge-intervals/description/)

 * Set Matrix Zero: 
   * SC: brute -> O(n2) , better -> O(n) , best -> O(1) . Thinking O(1) is tricky
   * [LeetCode](https://leetcode.com/problems/set-matrix-zeroes/description/)  
   * [Striver Article](https://takeuforward.org/data-structure/set-matrix-zero/)  

  
 * Find element in array having frequency > floor(size/2): **Moore's voting algo**
   * When SC: O(1), then it is called Moore's voting algo. 
   * [LeetCode](https://leetcode.com/problems/majority-element/)  
   * [Striver Article](https://takeuforward.org/data-structure/find-the-majority-element-that-occurs-more-than-n-2-times/)
   * Similar problem is finding all the numbers having frequency greater than floor(size/3)
   * [LeetCode](https://leetcode.com/problems/majority-element-ii/)  
   * [Striver Article](https://takeuforward.org/data-structure/majority-elementsn-3-times-find-the-elements-that-appears-more-than-n-3-times-in-the-array/)
 
### Hard

 * 3 Sum: 
   * Kinda medium hard. If you know the logic behind the optimal solution, it becomes intuitive. Handling duplicates is also challenging
   * [LeetCode](https://leetcode.com/problems/3sum/description/)  
   * [Striver Article](https://takeuforward.org/data-structure/3-sum-find-triplets-that-add-up-to-a-zero/)  
   * [LeetCode](https://leetcode.com/problems/4sum/description/) -> Follow up question
   * [Striver Article](https://takeuforward.org/data-structure/4-sum-find-quads-that-add-up-to-a-target-value/)  

 * Count Inversions in an array:
   * Involves merge sort. The intution to think in that direction is not an easy task
   * [GFG](https://www.geeksforgeeks.org/problems/inversion-of-array-1587115620/1)  
   * [Striver Article](https://takeuforward.org/data-structure/count-inversions-in-an-array/)  
   * [LeetCode](https://leetcode.com/problems/reverse-pairs/) -> Follow up question
   * [Striver Article](https://takeuforward.org/data-structure/count-reverse-pairs/)  

## Bit Manipulation

### Easy

 * Find missing and repeating in array of 1-N:
   * A classic bit manipulation question
   * [Striver Article](https://takeuforward.org/data-structure/find-the-repeating-and-missing-numbers/)  
   * [GFG](https://www.geeksforgeeks.org/problems/find-missing-and-repeating2512/1) 

### Medium 

### Hard
