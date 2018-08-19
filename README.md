# Totient-

import math as m

n=int(input())
t=m.ceil(m.sqrt(n))

res=n
for x in range(2,t+1):
    
    if n%x==0:
        while n%x==0:
            n=n/x
        res*=1-(1/x)
          
if n>1:
    res*=1-(1/n)
print(round(res))
