# Day 2

Problem: Two sum
leetcode link: https://leetcode.com/problems/two-sum/

```js
//js solution
function twoSum(nums, target) {
  for (let i = 0; i < nums.length; i++) {
    for (let j = i + 1; j < nums.length; j++) {
      if (nums[i] + nums[j] === target) {
        return [i, j];
      }
    }
  }
}
```

Input:nums = [2,7,11,15], target = 9

Output: [0,1]

Algorithm: Brute Force

Python Solution:

```py
# solution here
def two_sum(nums, target):
    for i in range(len(nums)):
        for j in range(i + 1, len(nums)):
            if nums[i] + nums[j] == target:
                return [i, j]
```

Problem: Best Time to Buy and Sell Stock
leetcode link: https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/

```js
//js solution
```

Input: prices = [7,1,5,3,6,4]

Output: 5

Algorithm: Single Pass

Python Solution:

```py
# solution here
def max_profit(prices):
    min_price = float('inf')
    max_profit = 0

    for price in prices:
        if price < min_price:
            min_price = price
        elif price - min_price > max_profit:
            max_profit = price - min_price

    return max_profit
```
