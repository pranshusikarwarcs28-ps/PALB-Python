class Solution:
    def getMinDiff(self, arr, k):
        n = len(arr)
        arr.sort()
        
        # initial difference
        ans = arr[n-1] - arr[0]
        
        # initial smallest and largest after modification
        small = arr[0] + k
        big = arr[n-1] - k
        
        if small > big:
            small, big = big, small
        
        # check every split
        for i in range(n-1):
            
            # if height becomes negative → skip
            if arr[i+1] - k < 0:
                continue
            
            new_min = min(small, arr[i+1] - k)
            new_max = max(big, arr[i] + k)
            
            ans = min(ans, new_max - new_min)
        
        return ans
