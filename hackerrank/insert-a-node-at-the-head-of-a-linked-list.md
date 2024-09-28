# Insert a Node at the Head of a Linked List

This repository contains Python solutions for working with linked lists. This specific code focuses on inserting a new node with a given data value at the beginning (head) of a singly linked list.

## Problem Description

**Function:** `insertNodeAtHead(llist, data)`

This function takes the head node of a linked list (`llist`) and an integer (`data`) as input. It creates a new node, sets its data value, and inserts it at the front (head) of the linked list. The original head node becomes the second node in the list. The function returns the reference to the new head node of the modified list.

**Input:**

- `llist`: A reference to the head node of the linked list (may be `None` if the list is empty).
- `data`: The integer value to be inserted in the new node.

**Constraints:**

- The number of nodes inserted at the head can range from 1 to 1000.

**Output:**

The function returns the reference to the new head node of the modified linked list after inserting the new node at the head.


## Solution

### Python Code:

```python

def insertNodeAtHead(llist, data):
  new_node = SinglyLinkedListNode(data)
  if llist is None:
    return new_node  # Handle empty list case
  new_node.next = llist
  llist = new_node
  return llist

### Contact

Hackerrank:  <https://www.hackerrank.com/challenges/find-a-string/problem?isFullScreen=true> <br>
MY Account: <https://www.hackerrank.com/profile/krishnapatidar62><br>
Linkedin: <https://www.linkedin.com/in/krishna-patidar-kp/>