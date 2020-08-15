# Chocolate-distribution-problem

 Q)Given an array A of positive integers of size N, where each value represents number of chocolates in a packet. Each packet can have variable number of chocolates. There are M students, the task is to distribute chocolate packets such that :
 1. Each student gets one packet.
 2. The difference between the number of chocolates given to the students having packet with maximum chocolates and student having packet with minimum chocolates is minimum.

t=int(input())
for i in range(t):
    b=[]
    n=int(input())
    d=list(map(int,input().split()))
    st=int(input())
    a=sorted(d) 
    
    s=a[n-1]
    if(n!=st):
        for i in range(0,n-st+1):
            c=a[i+st-1]-a[i]
            if(c<s):
                s=c
            i+=1
        print(s)
    if(n==st):
        print(a[n-1]-a[0])
