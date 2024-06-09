# DSA Course
This repo contains all the questions which I found important in the striver DSA course [link](https://takeuforward.org/strivers-a2z-dsa-course/strivers-a2z-dsa-course-sheet-2)

---

The structure of the repo is as follows 
1. An appendix section contains some useful links for certain concepts
2. A H2 heading will contain the broad topic, for example - Arrays, Trees, Graphs, etc.
3. Each topic will have sub-headings. Each sub-heading will mean a different level for the question of that topic.
4. There will be a list of questions of each category level. It will contain the different links for that question, including videos, questions, articles, different solutions, etc.

**Each branch points to the topic**

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

### Hard
