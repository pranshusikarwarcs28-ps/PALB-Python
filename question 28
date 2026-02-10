class Solution:
    def factorial(self, N):
        res = [1]   # stores digits in reverse
        
        size = 1
        
        # multiply numbers from 2 to N
        for x in range(2, N+1):
            carry = 0
            
            for i in range(size):
                prod = res[i] * x + carry
                res[i] = prod % 10
                carry = prod // 10
            
            # handle remaining carry
            while carry:
                res.append(carry % 10)
                carry //= 10
                size += 1
        
        # reverse to get actual number
        return res[::-1]
