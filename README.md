I used geeksforgeeks article Complexity of Different Operations of Binary Tree, Binary Search Tree, and AVL Tree to see what the asymptotic complexity of search in a binary tree is. 
I used claude.ai to learn more about how algorithms might not run as fast in practice. 
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
- Asymptotic analysis may be misleading in actual performance due to hardware limitations, such as the amount of memory needed for recursive calls.
- Constant factors ignored in asymptotic analysis may be a significant enough factor to change performance significantly.
- The input may be the optimal input for the algorithm, allowing the runtime to be much lower than expected. 

Input Size Asymptotic Complexity
- Finding an element in a binary search tree of 1,000 elements could take 5 seconds. The same element in a tree of 10,000 elements will obviously take longer, but not by much. Search in an binary tree has the complexity of log(n), where n is the number of nodes. log(1000) = 3 where log(10,000) = 4 and log(100,000) = 5. Judging by how each solution changes by +1, and 1000 elements takes 5 seconds (3 * 2)-1 = 5, I would assume 10,000 elements takes (4 * 2)-1 = 7 seconds roughly. 

Increased Asymptotic Complexity
- The time could be quite longer than expected due to hardware errors such as memory fragmentation from repeated reallocation of current location inside the binary tree.
- The nodes themselves may require memory allocation which adds computational runtime, especially in a large input.
- If the algorithm was written recursively, the search may call an excessive amount of recursive calls, which exponentially increases runtime. 
