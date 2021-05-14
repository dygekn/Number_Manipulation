def num():
    n=input("Enter the number:")
    if max(n)>n[0]:
       a= n.replace(max(n),n[0])
       c="The largest number is:"
       print(c, max(n)+a[1:len(a)])
    if  ("0" in n ):           
       x=n.index("0")
       n = n[:x] + n[x+1:]
       q="The smallest number is:"
       y=n.replace(min(n),n[0])
       print(q,min(n)+y[1:x]+ "0"+y[x:len(y)])
    elif min(n)<n[0] : 
       b= n.replace(min(n),n[0])
       d="The smallest number is:"
       print(d,min(n)+b[1:len(b)])
       return n
                
num()
