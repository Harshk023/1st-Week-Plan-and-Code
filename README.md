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
