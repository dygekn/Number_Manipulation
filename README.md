# Number_Manipulation
def door(): 
    import random
    n1=0.10
    n2=0.20
    n3=0.30
    n4=0.10
    n5=0.30
    dict ={1:3,2:1,3:0,4:2,5:4}
    a=(n1*100) 
    b=(n2*100) 
    c=(n3*100) 
    d=(n4*100) 
    e=(n5*100) 
    numberofday=0
    while True:
        rdnt=random.randint(1, 100)
        if rdnt>=1 and rdnt<=a  :
            numberofday+= dict[1]
        elif rdnt>=a+1 and rdnt<=b+a :
            numberofday+= dict[2]
        elif rdnt>=b+a+1 and rdnt<=c+b+a:
            numberofday+= dict[3]
            break 
        elif rdnt>=c+a+b+1 and rdnt<=d+c+a+b:
            numberofday+= dict[4]
            break
        else:       
            numberofday+= dict[5]
    return numberofday     

import numpy as np


variance=[]
for i in range(20):
    x=door()
    variance.append(x)
print("When simulation n=20, variance is",np.var(variance))


variance=[]
for i in range(50):
    x=door()
    variance.append(x)
print("When simulation n=50, variance is",np.var(variance))



variance=[]
for i in range(100):
    x=door()
    variance.append(x)
print("When simulation n=100, variance is",np.var(variance))


variance=[]
for i in range(500):
    x=door()
    variance.append(x)
print("When simulation n=500, variance is",np.var(variance))


variance=[]
for i in range(1000):
    x=door()
    variance.append(x)
print("When simulation n=1000, variance is",np.var(variance))
