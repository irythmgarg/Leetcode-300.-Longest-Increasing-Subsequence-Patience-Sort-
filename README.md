# Leetcode-300.-Longest-Increasing-Subsequence-Patience-Sort-

# 📈 Longest Increasing Subsequence (LIS) Using Smart Replacement

## 🧩 Problem Statement

Given an integer array `nums`, return the length of the **longest strictly increasing subsequence**.

> Each subsequence must be strictly increasing but not necessarily contiguous.

### ✨ Example

```
Input: nums = [10,9,2,5,3,7,101,18]
Output: 4
Explanation: The LIS is [2,3,7,101]
```

---

## 🧠 Approach: Smart Replacement Technique (Greedy + Modified Binary Search Concept)

### 🔍 Key Idea

Maintain an auxiliary list `arr` where:

* `arr[i]` stores the smallest tail of all increasing subsequences of length `i+1`.
* If `nums[i]` is larger than all elements, append it.
* Else, replace the first element in `arr` which is `>= nums[i]` (to maintain minimum tail).

This guarantees the potential for future longer subsequences.

> ✅ This is not the actual LIS but helps to find its length efficiently.

---

## ⚙️ Time Complexity

* **O(n²)** due to linear scan in `findy()`.

> Note: It can be optimized to **O(n log n)** using `lower_bound` from STL.

## 💾 Space Complexity

* **O(n)** for storing the `arr` vector.

---

## 🎨 Visual Walkthrough

```
nums: [10, 9, 2, 5, 3, 7, 101, 18]
arr:  [2, 3, 7, 18] -> after all processing
LIS Length = 4
```

---

## 🧑‍💻 Author Info

> ✍️ Made with 💡 by **Ridham Garg**
> 🎓 **Thapar Institute of Engineering and Technology**
> 📧 [Ridhamgarg000@gmail.com](mailto:Ridhamgarg000@gmail.com)

---

> 🚀 "Every number has its place — let's find the longest rising path!" 📶✨
