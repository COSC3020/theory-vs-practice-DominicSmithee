I used geeksforgeeks article Complexity of Different Operations of Binary Tree, Binary Search Tree, and AVL Tree to see what the asymptotic complexity of search in a binary tree is. 

# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

Answers:

Misleading Analysis
- Asymptotic analysis may be misleading in actual performance due to hardware limitations, such as the amount of threads that could be created on the machine might differ from what the algorithm requires.
- Constant factors ignored in asymptotic analysis may be a significant enough factor to change performance significantly.
- You might just be wrong about the found asymptotic analysis due to other factors, such as recursion being confusing and runtime analysis being generally difficult to grasp

Input Size Asymptotic Complexity
- Finding an element in a binary search tree of 1,000 elements could take 5 seconds. The same element in a tree of 10,000 elements will obviously take longer, but not by much. Search in an binary tree has the complexity of O(logn), where n is the number of nodes. O(log(1000)) = 3 where O(log(10,000)) = 4 and O(log(100,000)) = 5. Judging by how each solution changes by +1, and 1000 elements takes 5 seconds (3*2)-1 = 5, I would assume 10,000 elements takes (4*2)-1 = 7 seconds roughly. 
