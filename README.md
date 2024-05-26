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
    
* **Custom Sort** : If you want to swap, return `false`
  * [Luv](https://www.youtube.com/watch?v=3pvZhwp0U9w)
  * Most common method is to return the actual order you want. For example to sort an array in decreasing order `return num1 > num2;`
    
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
   * [Striver Article](https://takeuforward.org/arrays/longest-subarray-with-sum-k-postives-and-negatives/)  
   * [GFG](https://www.geeksforgeeks.org/problems/longest-sub-array-with-sum-k0809/1)  

  * 

### Hard
