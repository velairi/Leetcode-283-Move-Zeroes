# Move-Zeroes
Leetcode #283 Move Zeroes

Given an array nums, write a function to move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Example:

Input: [0,1,0,3,12]
Output: [1,3,12,0,0]
Note:

You must do this in-place without making a copy of the array.
Minimize the total number of operations.

```
func moveZeroes(_ arr: inout [Int]) {
  var i = 0, j = 1
  while j < arr.count {
    if arr[i] == 0 && arr[j] != 0 {
      (arr[i], arr[j]) = (arr[j], arr[i])
    } else if arr[i] == 0 && arr[j] == 0 {
      j += 1
      continue
    } 
    i += 1
    j += 1
  }
}
```
