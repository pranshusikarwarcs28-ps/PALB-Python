class Solution:
    def commonElements(self, arr1, arr2, arr3):
        n1, n2, n3 = len(arr1), len(arr2), len(arr3)
        
        i = j = k = 0
        ans = []
        
        while i < n1 and j < n2 and k < n3:
            
            # all equal
            if arr1[i] == arr2[j] == arr3[k]:
                ans.append(arr1[i])
                val = arr1[i]
                
                # skip duplicates
                while i < n1 and arr1[i] == val:
                    i += 1
                while j < n2 and arr2[j] == val:
                    j += 1
                while k < n3 and arr3[k] == val:
                    k += 1
            
            # move smallest pointer
            elif arr1[i] < arr2[j]:
                i += 1
            elif arr2[j] < arr3[k]:
                j += 1
            else:
                k += 1
        
        if not ans:
            return [-1]
        
        return ans
