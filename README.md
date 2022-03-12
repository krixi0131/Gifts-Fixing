# Gifts-Fixing
```python
t=int(input())
for count in range(t):
    n=int(input())
    a=list(map(int,input().split()))
    b=list(map(int,input().split()))
    mi=10**9
    me=10**9
    ans=0
    for i in range(n):
        if a[i]<mi:
            mi=a[i]
        if b[i]<me:
            me=b[i]
    for i in range(n):
        if (a[i]-mi)>(b[i]-me):
            ans+=(b[i]-me)
            ans+=(a[i]-mi-b[i]+me)
        else:
            ans+=(a[i]-mi)
            ans+=b[i]-me-a[i]+mi
    print(ans)
        
```
