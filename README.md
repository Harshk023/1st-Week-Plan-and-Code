🚀 1st-Week-Plan-and-Code
A structured 7-day roadmap covering Python basics, arrays, strings, and LeetCode problem solutions. Includes theory notes, clean code snippets, and practice problems to help beginners build strong DSA fundamentals.

| Day       | Focus Area & Questions                                                                                    |
| --------- | --------------------------------------------------------------------------------------------------------- |
| **Day 1** | Python Basics – *Loops, Lists, Sets, Dictionaries, Input/Output, Functions*                               |
| **Day 2** | Big‑O notation & basic array operations                                                                   |
| **Day 3** | **LeetCode #1920 – Build Array from Permutation**                                                         |
| **Day 4** | **LeetCode #303 – Range Sum Query: Immutable** <br> **LeetCode #238 – Product of Array Except Self**      |
| **Day 5** | **LeetCode #344 – Reverse String** <br> **LeetCode #125 – Valid Palindrome**                              |
| **Day 6** | **LeetCode #167 – Two Sum II (Input Array Is Sorted)** <br> **LeetCode #977 – Squares of a Sorted Array** |
| **Day 7** | Mixed practice: 5–6 easy problems (arrays & strings)                                                      |


📅 Day 1 – Python Basics
🎯 Objective
Master the foundational Python concepts needed for solving Data Structures and Algorithms (DSA) problems effectively.

✅ Topics to Cover
🔄 Loops: for, while, range(), and control statements (break, continue, pass)
📜 Lists: Creating, accessing elements, methods (append(), pop(), sort(), reverse()), slicing, list comprehension
🔹 Sets: Unique elements, operations (union(), intersection(), difference())
🔑 Dictionaries: Key-value pairs, adding, updating, deleting keys, iteration
⌨ Input/Output: input(), reading multiple integers (map()), formatted printing (f"")
🛠 Functions: Defining functions, parameters, return values, default & keyword arguments

💻 Example Code
def sum_of_evens(nums):
    total = 0
    for n in nums:
        if n % 2 == 0:
            total += n
    return total

print(sum_of_evens([1, 2, 3, 4, 5, 6]))  # Output: 12


"""
DAY - 2 : Big-O Notation & Basic Array Operations
---------------------------------------
Author: [Your Name]
Date: [Today's Date]

This file explains:
1. What Big-O notation is.
2. How common array operations work.
3. The time complexity (Big-O) of each operation.

Big-O notation helps us measure how the runtime or memory usage
of an algorithm grows as the size of the input grows.

We focus on the *worst-case* scenario.
"""

# Let's use Python lists to represent arrays
arr = [10, 20, 30, 40, 50]

# ----------------------------------------------------
# 1. Accessing an element (O(1) - Constant Time)
# ----------------------------------------------------
# Accessing any index in an array is O(1) because
# it takes the same time regardless of the array size.
print("Access element at index 2:", arr[2])  # Output: 30

# ----------------------------------------------------
# 2. Searching for an element (O(n) - Linear Time)
# ----------------------------------------------------
# In the worst case, we might have to check every element.
def linear_search(array, target):
    for i in range(len(array)):
        if array[i] == target:
            return i
    return -1

print("Search for 40:", linear_search(arr, 40))  # Output: 3
print("Search for 100:", linear_search(arr, 100))  # Output: -1

# ----------------------------------------------------
# 3. Inserting an element at the end (O(1) - Amortized)
# ----------------------------------------------------
# Appending is usually O(1), unless Python needs to
# resize the underlying list.
arr.append(60)
print("After appending 60:", arr)

# ----------------------------------------------------
# 4. Inserting an element at the beginning (O(n))
# ----------------------------------------------------
# Inserting at the start requires shifting all elements.
arr.insert(0, 5)
print("After inserting 5 at start:", arr)

# ----------------------------------------------------
# 5. Deleting an element (O(n))
# ----------------------------------------------------
# Deleting from the middle/start requires shifting elements.
arr.remove(30)  # Removes the first occurrence of 30
print("After removing 30:", arr)

# ----------------------------------------------------
# 6. Traversing the array (O(n))
# ----------------------------------------------------
# Visiting each element once.
def traverse(array):
    for element in array:
        print(element, end=" ")
    print()

print("Traversing array:", end=" ")
traverse(arr)

# ----------------------------------------------------
# Summary of Time Complexities:
# ----------------------------------------------------
# Operation                  Time Complexity
# -------------------------------------------
# Access by index            O(1)
# Search (unsorted)          O(n)
# Insert at end              O(1) amortized
# Insert at beginning/middle O(n)
# Delete by value/index      O(n)
# Traverse                   O(n)
# ----------------------------------------------------

