# DP

[1048. Longest String Chain](https://leetcode.cn/problems/longest-string-chain/)

You are given an array of `words` where each word consists of lowercase English letters.

`wordA` is a **predecessor** of `wordB` if and only if we can insert **exactly one** letter anywhere in `wordA` **without changing the order of the other characters** to make it equal to `wordB`.

- For example, `"abc"` is a **predecessor** of `"abac"`, while `"cba"` is not a **predecessor** of `"bcad"`.

A **word chain** is a sequence of words `[word1, word2, ..., wordk]` with `k >= 1`, where `word1` is a **predecessor** of `word2`, `word2` is a **predecessor** of `word3`, and so on. A single word is trivially a **word chain** with `k == 1`.

Return *the **length** of the **longest possible word chain** with words chosen from the given list of* `words`.

 

```python
class Solution:
    def longestStrChain(self, words: List[str]) -> int:
        cnt = defaultdict(int)
        words.sort(key=len)
        res = 0
        for word in words:
            cnt[word] = 1
            for i in range(len(word)):
                prev = word[:i] + word[i+1:]
                if prev in cnt:
                    cnt[word] = max(cnt[word], cnt[prev] + 1)
            res = max(res, cnt[word])
        return res
```



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

