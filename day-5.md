# Day 5

Problem: Palindrome number
leetcode link: https://leetcode.com/problems/palindrome-number/

```js
//js solution
function isPalindrome(x) {
  if (x < 0) return false;
  const str = x.toString();
  let left = 0;
  let right = str.length - 1;
  while (left < right) {
    if (str[left] !== str[right]) return false;
    left++;
    right--;
  }
  return true;
}
```

Input: x = 121

Output: True

Algorithm: Two Pointer

Python Solution:

```py
# solution here
def is_palindrome(x):
    if x < 0:
        return False

    s = str(x)
    left = 0
    right = len(s) - 1

    while left < right:
        if s[left] != s[right]:
            return False
        left += 1
        right -= 1

    return True
```
