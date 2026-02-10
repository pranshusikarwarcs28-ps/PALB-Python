class Solution:
    def nextGap(self, gap):
        if gap <= 1:
            return 0
        return (gap // 2) + (gap % 2)

    def mergeArrays(self, a, b):
        n = len(a)
        m = len(b)
        
        gap = self.nextGap(n + m)

        while gap > 0:
            i = 0
            j = gap

            while j < n + m:
                
                # case 1: both in a
                if i < n and j < n:
                    if a[i] > a[j]:
                        a[i], a[j] = a[j], a[i]

                # case 2: i in a, j in b
                elif i < n and j >= n:
                    if a[i] > b[j - n]:
                        a[i], b[j - n] = b[j - n], a[i]

                # case 3: both in b
                else:
                    if b[i - n] > b[j - n]:
                        b[i - n], b[j - n] = b[j - n], b[i - n]

                i += 1
                j += 1

            gap = self.nextGap(gap)
