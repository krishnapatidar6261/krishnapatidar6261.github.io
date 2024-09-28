# print-the-elements-of-a-linked-list

This repository contains a Python solution to practice traversing a linked list. The goal is to print each node's data element from the linked list, with each value printed on a new line.

## Problem Description

### Task:
Given a pointer to the head node of a linked list, print each node's data value, one per line. If the head pointer is null (indicating the list is empty), there is nothing to print.

### Input Format:
1. The first line of input contains an integer `n`, the number of elements in the linked list.
2. The next `n` lines each contain one integer, the data values for each node.

### Constraints:
- \( 1 \leq n \leq 1000 \)
- \( 1 < list[i] < 1000 \), where `list[i]` is the `i`th element of the linked list.

### Sample Input:
2 
16
13

### Sample Output:
16 
13


### Explanation:
There are two elements in the linked list, represented as `16 -> 13 -> NULL`. The `printLinkedList` function should print `16` and `13` each on a new line.

## Solution

### Python Code:

```python

def printLinkedList(head):
    if head is None:
        return None

    curr_pos = head
    while curr_pos is not None:
        print(curr_pos.data)
        curr_pos = curr_pos.next


### Contact

Hackerrank:  <https://www.hackerrank.com/challenges/find-a-string/problem?isFullScreen=true> <br>
MY Account: <https://www.hackerrank.com/profile/krishnapatidar62><br>
Linkedin: <https://www.linkedin.com/in/krishna-patidar-kp/>