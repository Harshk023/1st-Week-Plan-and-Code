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




"""
DAY 3: Reverse Array, Max/Min Element Problems
Author: [Your Name]
Date: [Today's Date]

Topics Covered:
1. Reverse an array
2. Find maximum and minimum elements in an array
3. LeetCode #1920 - Build Array from Permutation
4. LeetCode #1299 - Replace Elements with Greatest Element on Right Side
"""

# ----------------------------------------------------
# 1. Reverse an Array (O(n))
# ----------------------------------------------------
# Problem: Given an array, reverse it in-place.

def reverse_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left += 1
        right -= 1
    return arr

arr1 = [1, 2, 3, 4, 5]
print("Original:", arr1)
print("Reversed:", reverse_array(arr1))


# ----------------------------------------------------
# 2. Find Maximum and Minimum Elements (O(n))
# ----------------------------------------------------
# Problem: Given an array, find the maximum and minimum values.

def find_max_min(arr):
    max_val = arr[0]
    min_val = arr[0]
    for num in arr:
        if num > max_val:
            max_val = num
        if num < min_val:
            min_val = num
    return max_val, min_val

arr2 = [12, 4, 19, 33, 7]
max_val, min_val = find_max_min(arr2)
print(f"Array: {arr2}")
print(f"Max: {max_val}, Min: {min_val}")


# ----------------------------------------------------
# 3. LeetCode #1920 - Build Array from Permutation
# ----------------------------------------------------
"""
Problem:
Given a zero-based permutation nums (0-indexed), build an array ans where:
ans[i] = nums[nums[i]] for each 0 <= i < nums.length
and return it.

Example:
Input: nums = [0,2,1,5,3,4]
Output: [0,1,2,4,5,3]
"""

def build_array(nums):
    return [nums[nums[i]] for i in range(len(nums))]

nums_1920 = [0, 2, 1, 5, 3, 4]
print("LC #1920 Input:", nums_1920)
print("LC #1920 Output:", build_array(nums_1920))


# ----------------------------------------------------
# 4. LeetCode #1299 - Replace Elements with Greatest Element on Right Side
# ----------------------------------------------------
"""
Problem:
Given an array arr, replace every element with the greatest element among the elements to its right,
and replace the last element with -1.

Example:
Input: arr = [17,18,5,4,6,1]
Output: [18,6,6,6,1,-1]
"""

def replace_elements(arr):
    max_right = -1
    for i in range(len(arr) - 1, -1, -1):
        new_val = max_right
        if arr[i] > max_right:
            max_right = arr[i]
        arr[i] = new_val
    return arr

arr_1299 = [17, 18, 5, 4, 6, 1]
print("LC #1299 Input:", [17, 18, 5, 4, 6, 1])
print("LC #1299 Output:", replace_elements(arr_1299))


# ----------------------------------------------------
# Time Complexity Summary:
# ----------------------------------------------------
# Reverse array               O(n)
# Find max/min                O(n)
# LC #1920                    O(n)
# LC #1299                    O(n)
# ----------------------------------------------------


"""
Day 4: Prefix Sum Problems
Author: [Your Name]
Date: [Today's Date]

Topics Covered:
1. Understanding Prefix Sum
2. LeetCode #303 - Range Sum Query: Immutable
3. LeetCode #238 - Product of Array Except Self
"""

# ----------------------------------------------------
# 1. Understanding Prefix Sum
# ----------------------------------------------------
# Prefix sum is a technique where we precompute the sum of elements
# up to each index so that we can answer range sum queries quickly.

def prefix_sum_array(nums):
    prefix = [0] * (len(nums) + 1)  # Extra space for sum[0] = 0
    for i in range(len(nums)):
        prefix[i + 1] = prefix[i] + nums[i]
    return prefix

arr = [2, 4, 6, 8]
print("Array:", arr)
print("Prefix Sum:", prefix_sum_array(arr))
# prefix[i] = sum of arr[0] to arr[i-1]


# ----------------------------------------------------
# 2. LeetCode #303 - Range Sum Query: Immutable
# ----------------------------------------------------
"""
Problem:
Given an integer array nums, handle multiple queries of the form:
sumRange(i, j) = sum of nums between indices i and j (inclusive).

Example:
Input: nums = [-2, 0, 3, -5, 2, -1]
Queries: sumRange(0, 2) -> 1
         sumRange(2, 5) -> -1
         sumRange(0, 5) -> -3

Approach:
1. Precompute prefix sums.
2. Answer each query in O(1) time.

Time Complexity:
- Precomputation: O(n)
- Query: O(1)
"""

class NumArray:
    def __init__(self, nums):
        self.prefix = [0] * (len(nums) + 1)
        for i in range(len(nums)):
            self.prefix[i + 1] = self.prefix[i] + nums[i]

    def sumRange(self, left, right):
        return self.prefix[right + 1] - self.prefix[left]

# Example usage:
nums_303 = [-2, 0, 3, -5, 2, -1]
obj = NumArray(nums_303)
print("LC #303 sumRange(0,2):", obj.sumRange(0, 2))  # 1
print("LC #303 sumRange(2,5):", obj.sumRange(2, 5))  # -1
print("LC #303 sumRange(0,5):", obj.sumRange(0, 5))  # -3


# ----------------------------------------------------
# 3. LeetCode #238 - Product of Array Except Self
# ----------------------------------------------------
"""
Problem:
Given an array nums, return an array answer such that:
answer[i] = product of all nums except nums[i].

Example:
Input: nums = [1,2,3,4]
Output: [24,12,8,6]

Constraints:
- O(n) time
- Without using division

Approach:
1. Compute prefix products.
2. Compute suffix products.
3. Multiply prefix[i] * suffix[i] for each index.

Time Complexity: O(n)
Space Complexity: O(1) extra (excluding output)
"""

def productExceptSelf(nums):
    n = len(nums)
    answer = [1] * n

    # Prefix product
    prefix = 1
    for i in range(n):
        answer[i] = prefix
        prefix *= nums[i]

    # Suffix product
    suffix = 1
    for i in range(n - 1, -1, -1):
        answer[i] *= suffix
        suffix *= nums[i]

    return answer

nums_238 = [1, 2, 3, 4]
print("LC #238 Input:", nums_238)
print("LC #238 Output:", productExceptSelf(nums_238))


# ----------------------------------------------------
# Time Complexity Summary:
# ----------------------------------------------------
# Prefix sum computation        O(n)
# LC #303 Preprocessing         O(n), Query O(1)
# LC #238 Product except self   O(n)
# ----------------------------------------------------

"""
Day 5: String Basics, Reversing, Palindrome Check
Author: [Your Name]
Date: [Today's Date]

Topics Covered:
1. String basics in Python
2. Reverse a string
3. Palindrome check
4. LeetCode #344 - Reverse String
5. LeetCode #125 - Valid Palindrome
"""

# ----------------------------------------------------
# 1. String Basics in Python
# ----------------------------------------------------
# Strings are immutable in Python (cannot be changed in place).
# Common operations: slicing, concatenation, iteration.

sample_str = "Hello"
print("String:", sample_str)
print("First char:", sample_str[0])
print("Length:", len(sample_str))
print("Substring (1:4):", sample_str[1:4])

# ----------------------------------------------------
# 2. Reverse a String (O(n))
# ----------------------------------------------------
def reverse_string(s):
    return s[::-1]  # Python slicing trick

str1 = "Python"
print("Original:", str1)
print("Reversed:", reverse_string(str1))

# ----------------------------------------------------
# 3. Palindrome Check (O(n))
# ----------------------------------------------------
# A palindrome is a string that reads the same forward and backward.
def is_palindrome(s):
    return s == s[::-1]

print("Is 'madam' palindrome?", is_palindrome("madam"))
print("Is 'hello' palindrome?", is_palindrome("hello"))

# ----------------------------------------------------
# 4. LeetCode #344 - Reverse String
# ----------------------------------------------------
"""
Problem:
Write a function that reverses a string. The input string is given as a list of characters s.
Modify s in-place with O(1) extra memory.

Example:
Input: s = ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
"""

def reverseString(s):
    left, right = 0, len(s) - 1
    while left < right:
        s[left], s[right] = s[right], s[left]
        left += 1
        right -= 1

chars_344 = ["h", "e", "l", "l", "o"]
reverseString(chars_344)
print("LC #344 Output:", chars_344)

# ----------------------------------------------------
# 5. LeetCode #125 - Valid Palindrome
# ----------------------------------------------------
"""
Problem:
A phrase is a palindrome if, after converting all uppercase letters into lowercase letters
and removing all non-alphanumeric characters, it reads the same forward and backward.

Example:
Input: "A man, a plan, a canal: Panama"
Output: true
"""

def isPalindrome(s):
    filtered = [ch.lower() for ch in s if ch.isalnum()]
    return filtered == filtered[::-1]

print("LC #125:", isPalindrome("A man, a plan, a canal: Panama"))  # True
print("LC #125:", isPalindrome("race a car"))  # False

# ----------------------------------------------------
# Time Complexity Summary:
# ----------------------------------------------------
# Reverse string slicing         O(n)
# Palindrome check                O(n)
# LC #344                         O(n)
# LC #125                         O(n)
# ----------------------------------------------------
