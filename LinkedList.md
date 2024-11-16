# Inserting at the Beginning in a Linked List

## Concept
Inserting at the beginning means adding a new node such that:

1. The new node becomes the first node in the list.
2. The `next` pointer of the new node points to the old head node.
3. Finally, the head of the list is updated to this new node.

---

## Code

```python
class Node:
    def __init__(self, data):
        self.data = data  # Store the data
        self.next = None  # Initialize the next pointer as None

class LinkedList:
    def __init__(self):
        self.head = None  # Initialize the linked list with no nodes

    def insert_at_beginning(self, data):
        # Step 1: Create a new node
        new_node = Node(data)
        # Step 2: Point the new node's next to the current head
        new_node.next = self.head
        # Step 3: Update the head to the new node
        self.head = new_node
