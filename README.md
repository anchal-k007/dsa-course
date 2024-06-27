# DSA Course
This repo contains all the questions which I found important in the striver DSA course [link](https://takeuforward.org/strivers-a2z-dsa-course/strivers-a2z-dsa-course-sheet-2)

---

The structure of the repo is as follows 
1. An appendix section contains some useful links for certain concepts
2. A H2 heading will contain the broad topic, for example - Arrays, Trees, Graphs, etc.
3. Each topic will have sub-headings. Each sub-heading will mean a different level for the question of that topic.
4. There will be a list of questions of each category level. It will contain the different links for that question, including videos, questions, articles, different solutions, etc.

**Each branch points to the corresponding topic**

## Binary Search

### Easy

 * Find Mininum In A Rotated Sorted Array:
   * A classic BS question. Finding which portion to remove is the key problem
   * [Striver Article](https://takeuforward.org/data-structure/minimum-in-rotated-sorted-array/)  
   * [LeetCode](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/description/)
   * This is the follow up question, in which there duplicate values present in the array as well
   * [LeetCode](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array-ii/description/) 

 * Search In A Rotated Sorted Array:
   * A classic BS question. Finding which portion to remove is the key problem
   * There are 2 implementations
     * Find the minimum element in the array, using BS, and then perform the actual BS to search. Have this implemented here [LeetCode Submission](https://leetcode.com/problems/search-in-rotated-sorted-array/submissions/752863779/)
     * Remove the part of the array in which we know the array won't be sorted. This is the approach explained in Striver's article 
   * [Striver Article](https://takeuforward.org/data-structure/search-element-in-a-rotated-sorted-array/)  
   * [LeetCode](https://leetcode.com/problems/search-in-rotated-sorted-array/description/)
   * This is the follow up question, in which there duplicate values present in the array as well
   * [Striver Article](https://takeuforward.org/data-structure/search-element-in-a-rotated-sorted-array-ii/)  
   * [LeetCode](https://leetcode.com/problems/search-in-rotated-sorted-array-ii/description/) 

### Medium 

 * Koko Eating Bananas: **Problems involving reduction of search space based on answers**
   * This is one of the many questions where Binary Search on answers is applied. The aim is to remove one end of the search space. Typically, these type of questions can be identified by terms such as **minimum of possible values** or vice versa. Another hint which we can take is that before a particular value answers are not possible, but after that, all values are possible. This means that the search space can be divided into solution possible and not possible, where corresponding values are sorted. 
   * [LeetCode](https://leetcode.com/problems/koko-eating-bananas/description/)  
   * [Striver Article](https://takeuforward.org/binary-search/koko-eating-bananas/)
   * Other similar questions
   * [LeetCode: Minimum Days to make m bouquets](https://leetcode.com/problems/minimum-number-of-days-to-make-m-bouquets/description/) [Article](https://takeuforward.org/arrays/minimum-days-to-make-m-bouquets/)
   * [LeetCode: Find smallest divisor given a threshold](https://leetcode.com/problems/find-the-smallest-divisor-given-a-threshold/description/) [Article](https://takeuforward.org/arrays/find-the-smallest-divisor-given-a-threshold/)
   * [LeetCode: Capacity to ship packages within d days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/description/) [Article](https://takeuforward.org/arrays/capacity-to-ship-packages-within-d-days/)
   * [LeetCode: Split array largest sum](https://leetcode.com/problems/split-array-largest-sum/description/) [Article](https://takeuforward.org/arrays/split-array-largest-sum/)
   * [GFG: Allocate Minimum number of pages](https://www.geeksforgeeks.org/problems/allocate-minimum-number-of-pages0937/1) [Article](https://takeuforward.org/data-structure/allocate-minimum-number-of-pages/)
   * [GFG: Aggresive Cows](https://www.geeksforgeeks.org/problems/aggressive-cows/0) [Article](https://takeuforward.org/data-structure/aggressive-cows-detailed-solution/)

 * Search An Element In a Matrix Sorted row and column wise:
   * [LeetCode](https://leetcode.com/problems/search-a-2d-matrix/description/)  
   * [Striver Article](https://takeuforward.org/data-structure/search-in-a-sorted-2d-matrix/)
   * The follow up question (mentioned in the hard section) is follows the same concept, but needs a bit of trick to apply
  
### Hard
  
 * Kth missing Number In a sorted Array:
   * The brute force approach is straight-forward. Optimising it to BS requires that we involve the index of the values as well, which is not so intuitive if the approach is not known. 
   * [LeetCode](https://takeuforward.org/arrays/kth-missing-positive-number/)  
   * [Striver Article](https://takeuforward.org/arrays/kth-missing-positive-number/)  
   
 * Median Of 2 Sorted Arrays:
   * This question is a classic. Again, applying BS without using extra space is not so intuitive
   * [LeetCode](https://leetcode.com/problems/median-of-two-sorted-arrays/)  
   * [Striver Article](https://takeuforward.org/data-structure/median-of-two-sorted-arrays-of-different-sizes/)  

 * Search An Element In a Matrix Sorted row wise:
   * Doing it in O(nlogm) or O(mlogn) is not that difficult, but doing it in O(log(m+n)) requires thinking from a different direction
   * [LeetCode](https://leetcode.com/problems/search-a-2d-matrix-ii/description/)  
   * [Striver Article](https://takeuforward.org/arrays/search-in-a-row-and-column-wise-sorted-matrix/)


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
