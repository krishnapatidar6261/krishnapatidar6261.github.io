# Insert a Node at the Tail of a Linked List

This repository contains Python solutions for working with linked lists. This specific code focuses on inserting a new node with a given data value at the tail of a singly linked list.

## Problem Description

**Function:** `insertNodeAtTail(head, data)`

This function takes the head node of a linked list (`head`) and an integer (`data`) as input. It creates a new node with the provided data, inserts it at the end (tail) of the linked list, and returns the head node of the modified list. 

**Input:**

- `head`: A reference to the head node of the linked list (may be `None` if the list is empty).
- `data`: The integer value to be inserted in the new node.

**Constraints:**

- The number of nodes in the linked list can range from 1 to 1000.
- The data value of each node lies between 1 and 1000 (exclusive).

**Output:**

The function returns the reference to the head node of the modified linked list after inserting the new node at the tail.


## Solution

### Python Code:

```python
def insertNodeAtTail(head, data):
        new_node = SinglyLinkedListNode(data)
        if head is None:
          head = new_node
          return head
        curr_pos = head
        while curr_pos.next != None:
          curr_pos = curr_pos.next
        curr_pos.next = new_node
        return head

# Example usage (assuming `printLinkedList` function exists)
llist_count = int(input())
llist = SinglyLinkedList()

for _ in range(llist_count):
  llist_item = int(input())
  llist.insert_node(llist_item)   


llist.head = insertNodeAtTail(llist.head, new_data)  # Insert new data at tail
printLinkedList(llist.head)


### Contact

Hackerrank:  <https://www.hackerrank.com/challenges/find-a-string/problem?isFullScreen=true> <br>
MY Account: <https://www.hackerrank.com/profile/krishnapatidar62><br>
Linkedin: <https://www.linkedin.com/in/krishna-patidar-kp/>