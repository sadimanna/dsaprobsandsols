# Two Sum

> Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. 
> You may assume that each input would have exactly one solution, and you may not use the same element twice. 
> You can return the answer in any order.

> Runtime 0ms | Memory 13.17MB

```python
class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        nmap = {}
        for i in range(len(nums)):
            rem = target - nums[i]
            # print(rem)
            if rem not in nmap:
                nmap[nums[i]] = i
            else:
                return [nmap[rem], i]
            # print(nmap)
        return None
```
