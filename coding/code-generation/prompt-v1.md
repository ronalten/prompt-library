### **Prompt: Function Generator**

**Objective:** Generate a complete function based on a clear specification and requirements.

**Prompt:**
```
Create a Python function that takes a list of integers and returns a dictionary with the count of each unique number. The function should handle empty lists and be optimized for performance.
```

**Example Output:**
```python
from collections import Counter

def count_unique_numbers(nums):
    """
    Count occurrences of each unique integer in the list.

    Args:
        nums (list[int]): List of integers.

    Returns:
        dict: Dictionary with integers as keys and their counts as values.
    """
    return dict(Counter(nums))
```
