# 13-05-22-ass-2
import math
class Solution(object):
    def countPrimes(self,n):
        """
        :type n: int
        :rtype: int
        """
        arr=[True for i in range(n)]
        if n==0 or n==1:
            return 0
        arr[0]=False
        arr[1]=False
        x=int(math.sqrt(n))
        for i in range(2,x+1):
            if arr[i]==True:
                for j in range(i*i,n,i):
                    arr[j]=False
        ct=[i for i in arr if i == True]
        return len(ct)
        
output:
Your input- 10
Output -4
Expected-4
