Copy List with Random Pointer - Java Solution
An efficient implementation of the Copy List with Random Pointer problem using the Interweaving Technique in Java.
Problem Description
A linked list is given such that each node contains an additional random pointer, which could point to any node in the list or null. The goal is to construct a deep copy of the list where none of the pointers in the new list point to nodes in the original list.
Solution Approach
This solution avoids extra space (like a HashMap) by using a three-step pointer manipulation strategy:
Interweaving: Create a copy of each node and insert it directly after the original node (e.g., A -> A' -> B -> B').
Random Pointer Assignment: Set the random pointer of each copied node curr.next to curr.random.next.
Separation: Extract the copied nodes to form the new list while restoring the original list to its initial state.
Complexity
Time Complexity: O(n) – Performs three linear passes over the list.
Space Complexity: O(1) – No auxiliary data structures are used; only the memory for the new nodes is allocated.
