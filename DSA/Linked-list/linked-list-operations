# Singly Linked List Implementation

## Overview

A singly linked list is a fundamental data structure consisting of a sequence of nodes. Each node contains two components: data and a reference (or pointer) to the next node in the sequence. This project provides an implementation of a singly linked list in [language], offering functionalities such as insertion, deletion, and searching.

## Functionality

### Insertion

- **Insertion at the beginning:** Insert a new node with the provided data at the beginning of the list.
- **Insertion at the end:** Append a new node with the provided data at the end of the list.
- **Insertion at a specific position:** Insert a new node with the provided data at the specified position in the list.

### Deletion

- **Deletion at the beginning:** Remove the first node from the list.
- **Deletion at the end:** Remove the last node from the list.
- **Deletion of a specific node:** Remove a node with the specified data from the list.

### Searching

- **Searching for an element:** Search for a specific element within the list.

## Time Complexity

- **Insertion and deletion at the beginning:** O(1)
- **Insertion and deletion at the end (with tail pointer):** O(1)
- **Insertion and deletion at the end (without tail pointer):** O(n)
- **Insertion and deletion at a specific position:** O(n)
- **Searching:** O(n)

## Usage in diffrent Applications

Singly linked lists are commonly used in various applications, including:

1. **Dynamic Memory Allocation**: Singly linked lists are used in languages like C and C++ to implement dynamic memory allocation mechanisms like malloc() and free().
   
2. **Stacks and Queues**: Singly linked lists can be used to implement both stacks and queues efficiently.

3. **File Systems**: In file systems, linked lists can be used to maintain the list of blocks or sectors allocated to a file.

4. **Graphs**: Singly linked lists can be used to represent adjacency lists in graph implementations.

5. **Hash Tables**: In hash tables, linked lists are used to handle collisions, where multiple keys hash to the same index.


## Usage program

1. Clone this repository to your local machine.
2. Include the SinglyLinkedList class in your project.
3. Create a SinglyLinkedList object.
4. Use the provided methods to manipulate the list as needed.

## Requirements

Before running this program, ensure you have the following dependencies installed:

- Python 3.x
- Visual Studio Code (or any other code editor of your choice)

## Program Output

```python
class Node:

    def __init__(self,value):

        self.data=value
        self.next=None



class LinkedList(Node):

    def __init__(self):

        self.head=None
        self.n=0

#*************Create and insert Operations*********************************************
    #add element on first Head
    def head_append(self,value):

        new_node=Node(value)

        if self.n == 0:
            self.head=new_node

            return
        
        new_node.next=self.head

        self.head=new_node

        # to increate the length of list  
        self.n=self.n+1
        
    # add element at the end
    # add element on tail
    def append(self,value):

        new_node=Node(value)

        if self.n == 0:

            self.head=new_node
            self.n = self.n+1
            return
        
        last_node=self.head

        while last_node.next !=None:

            last_node=last_node.next

        last_node.next=new_node
        self.n=self.n+1

    # insert after the value
    def insert_after(self,pos,value):

        new_node=Node(value)

        cur_pos=self.head

        while cur_pos != None:
            
            if cur_pos.data==pos:
                break

            cur_pos=cur_pos.next

        '''
        There are a two condition if pos_after is found else not found 
        '''

        if cur_pos != None:
            new_node.next = cur_pos.next

            cur_pos.next=new_node

            self.n=self.n+1
        else:

            return "Item Not Found"


#***************print operation ********************************************
    def __str__(self):

        result=''

        last_node=self.head

        while last_node != None:
            

            result=result + str(last_node.data)+"-->"
            last_node=last_node.next

        if self.n == 0:

            return "Emplty List"
        
        return result[:-3]
    
#*************length Operations*************************************
    def __len__(self):

        return self.n

#***********************Delete Operations***********************************************
    def clear(self):

        self.head=None
        self.n=0


    def delete_head(self):
        
        if self.head == None:

            return "Empty List"
        
        self.head=self.head.next

        self.n = self.n-1

    def delete_tail(self):

        if self.head == None :
            
            return
        
        curr_pos=self.head

        while curr_pos != None:

            if curr_pos.next.next == None:
                
                curr_pos.next=None

                self.n -= 1

                return
            
            curr_pos = curr_pos.next
        



    def delete_val(self,value):

        if self.head == None:

            print("Empty List")

            return
        
        if self.head.data == value:

            self.delete_head()

            return
        
        curr_pos = self.head
        while curr_pos.next != None:

            if curr_pos.next.data == value:

                break

            curr_pos=curr_pos.next

        if curr_pos.next ==  None:

            print(" Value Not Found ")

        else:

            curr_pos.next=curr_pos.next.next
            self.n -= 1

#**************searh Operations**************************
    #work like find method
    def value_to_index(self,value):
        
        index=0
        curr_pos=self.head
        
        while curr_pos != None:

            if curr_pos.data == value:

                return index
            
            curr_pos=curr_pos.next
            index += 1

        return -1

    #return  index to value

    #getitem magic method is autometically call when we use squrebraket near out obj 
    #example obj[]
    #index to value return

    def __getitem__(self,index):

        index_pos=0
        curr_pos= self.head
        
        while curr_pos != None :

            if index_pos == index:

                return curr_pos.data

            curr_pos=curr_pos.next
            index_pos +=1

        return "Index Out Of bound" 

        
        



obj=LinkedList()


obj.append(10)
obj.append(20)
obj.append(30)
obj.append(40)
obj.append(50)

print(obj)
print(len(obj))        

#search 
index=obj.value_to_index(30)
print(index)

#index to value
#indexing

val=obj[30]
print(val)
