### **Prompt: Code Explainer**

**Objective:** Provide a clear, comprehensive explanation of code functionality, including purpose, logic flow, and key concepts.

**Prompt:**
```
Explain the following Python code step by step, including what it does, how it works, and any important concepts or patterns used:

def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return -1
```

**Example Output:**
# Binary search — step-by-step explanation

## Purpose
Find the index of `target` in a **sorted** list `arr`. If `target` is present, return its index; otherwise return `-1`.

## Signature and I/O
- Input: `arr` (sequence of comparable items, **must be sorted in ascending order**), `target` (value to find).  
- Output: integer index of `target` in `arr`, or `-1` if not found.

## High-level flow
1. Set two pointers: `left` at start (`0`) and `right` at end (`len(arr) - 1`).
2. While the search interval is valid (`left <= right`):
   - Compute middle index `mid = (left + right) // 2`.
   - If `arr[mid] == target` → return `mid`.
   - If `arr[mid] < target` → discard left half by setting `left = mid + 1`.
   - Else (`arr[mid] > target`) → discard right half by setting `right = mid - 1`.
3. If loop finishes without finding `target`, return `-1`.

## Line-by-line explanation
- `left, right = 0, len(arr) - 1`  
  Initialize search bounds: `left` is the first index (0), `right` is the last index (`len(arr) - 1`).

- `while left <= right:`  
  Continue while there is at least one element in the search interval.

- `mid = (left + right) // 2`  
  Choose the middle index of the current interval. `//` is integer (floor) division.

- `if arr[mid] == target:`  
  If the middle element equals the target, return the index `mid`.

- `elif arr[mid] < target:`  
  If the middle element is less than the target, move `left` to `mid + 1`.

- `else:`  
  If the middle element is greater than the target, move `right` to `mid - 1`.

- `return -1`  
  If the loop exits, the target is not in the array.

## Loop invariant
At the start of each loop iteration, the target (if it exists) must lie within indices `[left, right]`. Each iteration halves the size of that interval.

## Complexity
- Time: **O(log n)** — each iteration halves the search interval.  
- Space: **O(1)** — constant number of variables.

## Important notes
- Requires sorted input.  
- If duplicates exist, returns one matching index (not necessarily the first/last).  
- Inclusive bounds prevent skipping elements.  
- Python avoids integer overflow in `mid` calculation.

## Example trace
Array `arr = [1, 3, 5, 7, 9]`, `target = 6`

1. `left = 0`, `right = 4`  
   `mid = 2`, `arr[2] = 5` → `5 < 6` → `left = 3`.

2. `left = 3`, `right = 4`  
   `mid = 3`, `arr[3] = 7` → `7 > 6` → `right = 2`.

3. `left = 3`, `right = 2` → loop ends → return `-1`.

Example where target is found: `target = 5` → `mid = 2`, `arr[2] == 5` → return `2`.