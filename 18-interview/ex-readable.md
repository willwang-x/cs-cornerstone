# Readable

``` python
class Solution:
    def sortColors(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        L, R = 0, len(nums) - 1  
        i = 0
        while i <= R:
            if nums[i] == 0:
                nums[L], nums[i] = nums[i], nums[L]
                i += 1
                L += 1
            elif nums[i] == 2:
                nums[R], nums[i] = nums[i], nums[R]
                R -= 1
            else: 
                i += 1
```

vs 

``` python 
# Time: O(n)
# Space: O(1)

class Solution(object):
    def sortColors(self, nums: List[int]) -> None:
        def is_head(num):
            return num == 0

        def is_tail(num):
            return num == 2

        head, tail = 0, len(nums) - 1
        i = 0 
        
        while i <= tail:
            if is_head(nums[i]):
                nums[i], nums[head] = nums[head], nums[i]
                head += 1
                i += 1
            elif is_tail(nums[i]):
                nums[i], nums[tail] = nums[tail], nums[i]
                tail -= 1
            else:
                i += 1  
```