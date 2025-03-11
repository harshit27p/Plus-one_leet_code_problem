# Plus One

## Problem Statement
You are given a **large integer** represented as an integer array `digits`, where each `digits[i]` is the **i-th digit** of the integer. The digits are ordered from **most significant** to **least significant** in left-to-right order. The integer **does not contain any leading zeros**.

The task is to increment the large integer by **one** and return the resulting array of digits.

## Examples

### Example 1:
**Input:**  
```python
 digits = [1,2,3]
```
**Output:**  
```python
[1,2,4]
```
**Explanation:** The array represents the integer `123`. Incrementing by one gives `124`, resulting in `[1,2,4]`.

### Example 2:
**Input:**  
```python
 digits = [4,3,2,1]
```
**Output:**  
```python
[4,3,2,2]
```
**Explanation:** The array represents the integer `4321`. Incrementing by one gives `4322`, resulting in `[4,3,2,2]`.

### Example 3:
**Input:**  
```python
 digits = [9]
```
**Output:**  
```python
[1,0]
```
**Explanation:** The array represents the integer `9`. Incrementing by one gives `10`, resulting in `[1,0]`.

## Constraints
- `1 <= digits.length <= 100`
- `0 <= digits[i] <= 9`
- `digits` does **not** contain any leading zeros.

## Approach
1. Start from the **last digit** and add **one**.
2. If the last digit becomes `10`, carry over `1` to the previous digit.
3. Repeat this process moving left, handling the carry.
4. If all digits are `9`, append `1` at the start (e.g., `[9,9,9]` → `[1,0,0,0]`).


## Complexity Analysis
- **Time Complexity:** `O(n)`, where `n` is the length of `digits`.
- **Space Complexity:** `O(1)`, as the modification is done in-place (except when a new digit is added).

## Usage
To use the function, simply call it with an array:
```python
 digits = [9,9,9]
 print(plusOne(digits))  # Output: [1,0,0,0]
```

## Related Topics
- Array Manipulation
- Carry Propagation
- Mathematical Operations



