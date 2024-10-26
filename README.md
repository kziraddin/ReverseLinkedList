# ReverseLinkedList

This Python script implements a solution to reverse a singly linked list. It's designed to work with HackerRank's environment and includes the necessary boilerplate code for input/output handling.

## Problem Description

Given the head of a singly linked list, the task is to reverse the list in-place and return the new head. The input list may be empty (null head).

**Example:**
- Input: 1 → 2 → 3 → NULL
- Output: 3 → 2 → 1 → NULL

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

## Input Format

1. The first line contains an integer `t`, the number of test cases.
2. For each test case:
   - The first line contains an integer `n`, the number of elements in the linked list.
   - The next `n` lines each contain an integer, representing the data values of the list elements.

## Constraints

- 1 ≤ t ≤ 10
- 1 ≤ n ≤ 1000
- 1 ≤ list[i] ≤ 1000, where list[i] is the i-th element in the list

## Usage

This script is designed to run in HackerRank's environment. To use it locally:

1. Ensure you have Python 3 installed.
2. Modify the input method to accept user input or read from a file.
3. Change the output method to print to console or write to a file.

## Data Structure

The linked list is implemented using the `SinglyLinkedListNode` class:

```python
class SinglyLinkedListNode:
    def __init__(self, node_data):
        self.data = node_data
        self.next = None
```

## Time and Space Complexity

- Time Complexity: O(n), where n is the number of nodes in the linked list
- Space Complexity: O(1), as the reversal is done in-place

