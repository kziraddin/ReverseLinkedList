# ReverseLinkedList

This Python program reverses a singly linked list in-place. Given a head pointer of a linked list, it changes each node's `next` pointer to reverse the order of the nodes.

## Problem

Reverse a singly linked list given the pointer to its head node. The head pointer can be `null`, indicating an empty list.

### Example
- **Input**: `1 → 2 → 3 → NULL`
- **Output**: `3 → 2 → 1 → NULL`

## Solution

The `reverse` function accepts a linked list's head node and reverses the list in-place by manipulating the `next` pointers.

### Approach
1. Initialize three pointers: `prev` (set to `None`), `current` (starting at the head), and `next_node` (to store the next node).
2. Traverse the linked list:
   - Store the next node in `next_node`.
   - Reverse `current.next` to point to `prev`.
   - Move `prev` and `current` one step forward.
3. Return `prev` as the new head of the reversed list.

### Complexity
- **Time**: O(n), where n is the number of nodes (one pass through the list).
- **Space**: O(1), only a constant amount of space is used.

## File Structure

- **Classes**:
  - `SinglyLinkedListNode`: Defines a node in the linked list.
  - `SinglyLinkedList`: Manages the list and allows node insertion.
- **Functions**:
  - `reverse`: Reverses the linked list.
  - `print_singly_linked_list`: Outputs list elements.

## Input/Output

### Input Format
1. An integer `t` for the number of test cases.
2. For each test case:
   - An integer `n`, the number of elements.
   - `n` integers representing the node values.

### Sample
- **Input**:


## Function Description

The main logic is implemented in the `reverse` function:

```python
def reverse(llist):
    prev = None
    current = llist
    while current:
        next_node = current.next
        current.next = prev
        prev = current
        current = next_node
    return prev
```

This function takes the head of a linked list as input and returns the head of the reversed list.

## Applications

Reversing a linked list is a fundamental operation with several practical applications:

1. **Undo Functionality**: In applications that require an undo feature, like text editors or graphic design software, a reversed linked list can efficiently store and retrieve previous states.

2. **Browser History**: Web browsers often use linked lists to store browsing history. Reversing this list allows for easy navigation of previously visited pages in reverse order.

3. **Data Processing**: In scenarios where data needs to be processed in reverse order, such as certain algorithms or data analysis tasks, reversing a linked list can be useful.

4. **Palindrome Check**: Reversing a linked list is a key step in determining if a linked list represents a palindrome.

5. **Memory-Efficient Reversal**: For large datasets stored as linked lists, in-place reversal is memory-efficient compared to creating a new reversed list.

6. **Algorithm Implementation**: Many complex algorithms, especially in graph theory and tree traversals, use the concept of reversing links or paths.

7. **Interview and Learning**: Reversing a linked list is a classic problem in computer science education and technical interviews, helping to assess understanding of data structures and pointer manipulation.



