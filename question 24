class Solution:
    def findDuplicate(self, nums):
        low = 1
        high = len(nums) - 1
        ans = -1
        
        while low <= high:
            mid = (low + high) // 2
            
            # count numbers <= mid
            count = 0
            for num in nums:
                if num <= mid:
                    count += 1
            
            if count > mid:
                ans = mid
                high = mid - 1
            else:
                low = mid + 1
        
        return ans
