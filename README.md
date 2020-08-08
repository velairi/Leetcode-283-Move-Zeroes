# Move-Zeroes
Leetcode #283 Move Zeroes

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
