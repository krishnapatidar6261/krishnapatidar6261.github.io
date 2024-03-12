# Singly Linked List

A singly linked list is a fundamental data structure in computer science used to store a sequence of elements. Each element in a singly linked list is called a node.

## Node Structure

Each node contains two parts:

- **Data:** This part stores the actual element.
- **Next pointer/reference:** This part stores the reference to the next node in the sequence.

Unlike arrays, singly linked lists do not have a fixed size, and memory allocation for nodes is dynamic. This allows for efficient insertion and deletion operations at any position in the list, as long as the position is known. However, accessing an element by index in a singly linked list is less efficient compared to arrays because you have to traverse the list from the beginning to reach the desired element.

## Requirements

Before running this program, ensure you have the following dependencies installed:

- Python 3.x
- Visual Studio Code (or any other code editor of your choice)


# Singly Linked List Creating and Inserting Data Implementation in Python

This Python program demonstrates the implementation of a singly linked list. It includes functionalities to:
- Append elements to the end of the list
- Append elements to the beginning of the list (head)
- Insert elements after a specified value

## Program Output

```python
class Node:

    def __init__(self, value):
        self.data = value
        self.next = None

class LinkedList(Node):

    def __init__(self):
        self.head = None
        self.n = 0

    # Add element at the beginning (Head)
    def head_append(self, value):
        new_node = Node(value)
        if self.n == 0:
            self.head = new_node
            return
        new_node.next = self.head
        self.head = new_node
        self.n += 1

    # Add element at the end (Tail)
    def append(self, value):
        new_node = Node(value)
        if self.n == 0:
            self.head = new_node
            self.n += 1
            return
        last_node = self.head
        while last_node.next is not None:
            last_node = last_node.next
        last_node.next = new_node
        self.n += 1

    # Insert element after a specified value
    def insert_after(self, pos, value):
        new_node = Node(value)
        cur_pos = self.head
        while cur_pos is not None:
            if cur_pos.data == pos:
                break
            cur_pos = cur_pos.next
        if cur_pos is not None:
            new_node.next = cur_pos.next
            cur_pos.next = new_node
            self.n += 1
        else:
            return "Item Not Found"

    def __str__(self):
        result = ''
        last_node = self.head
        while last_node is not None:
            result += str(last_node.data) + "-->"
            last_node = last_node.next
        return result[:-3]

    def __len__(self):
        return self.n

obj = LinkedList()
obj.append(10)
obj.append(20)


print(obj)
print(len(obj))

obj.head_append("hello")
print(obj)
print(len(obj))

obj.insert_after(10, 100)
print(obj)
print(len(obj))

''' Output:
10-->20
2

hello-->10-->20


hello-->10-->100-->20
4
'''
