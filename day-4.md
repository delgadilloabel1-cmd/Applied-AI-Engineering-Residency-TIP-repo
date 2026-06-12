# Day 4

Problem: Contains Duplicates
leetcode link: https://leetcode.com/problems/contains-duplicate/

```js
//js solution
javascript;
function containsDuplicate(nums) {
  const seen = new Set();
  for (let i = 0; i < nums.length; i++) {
    if (seen.has(nums[i])) {
      return true;
    }
    seen.add(nums[i]);
  }
  return false;
}
```

Input: [1,2,3,1]

Output: true

Algorithm: This solution uses a hash set to track previously seen elements.

Python Solution:

```py
# solution here
def contains_duplicate(nums):
    seen = set()

    for num in nums:
        if num in seen:
            return True
        seen.add(num)

    return False
```

Problem:Group Anagrams
leetcode link: https://leetcode.com/problems/group-anagrams/

```js
//js solution
function groupAnagrams(strs) {
  const map = {};
  for (let i = 0; i < strs.length; i++) {
    const key = strs[i].split("").sort().join("");
    if (map[key] === undefined) {
      map[key] = [];
    }
    map[key].push(strs[i]);
  }
  return Object.values(map);
}
```

Input: strs = [""]

Output: [[""]]

Algorithm: Hash Map / Directory

Python Solution:

```py
# solution here
def group_anagrams(strs):
    groups = {}

    for s in strs:
        key = ''.join(sorted(s))

        if key not in groups:
            groups[key] = []

        groups[key].append(s)

    return list(groups.values())
```
