# DP

[740. Delete and Earn](https://leetcode.cn/problems/delete-and-earn/)

You are given an integer array `nums`. You want to maximize the number of points you get by performing the following operation any number of times:

- Pick any `nums[i]` and delete it to earn `nums[i]` points. Afterwards, you must delete **every** element equal to `nums[i] - 1` and **every** element equal to `nums[i] + 1`.

Return *the **maximum number of points** you can earn by applying the above operation some number of times*.

```python
from collections import Counter
class Solution:
    def deleteAndEarn(self, nums: List[int]) -> int:
        c = Counter(nums)
        x = sorted(c.items()) # arr of num and cnt
        
        res_include = 0
        res_exclude = 0
        prev_num = -1

        for num, cnt in x:
            res_include, res_exclude = max(res_include, res_exclude) + num * cnt if abs(num - prev_num) != 1 else num * cnt + res_exclude, max(res_include, res_exclude)
            prev_num = num
        
        return max(res_include, res_exclude)
```

