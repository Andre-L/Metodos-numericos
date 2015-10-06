import math
import numpy as np
import matplotlib.pyplot as plt
n=0
cont=float(0)
def f(x):
    fun=(math.exp(-x))-x
    return fun
def h(x):
    fun2= (math.exp(-x))
    return fun2
print "|%-7s|%-15s|%-15s|%-11s|%-11s|"%("i","Xi","PFijo","ErrA","ErrT")
print "|%-7s|%-15s|%-11s|%-11s|%-11s|"%("-------","----------","---------------","-----------","-----------")
while(n<10):
    g=(math.exp(-cont))
    aprox=(math.exp(-n))
    err=abs((g-cont)/(g))*100
    erra=abs((0.5-g)/(g))*100
    cont=g
    n+=1
    print "|%-7d|%-15f|%-15e|%-11f|%-11f|"%(n,aprox,g,err,erra)
    
x=np.arange(-2,2,0.1)
y=np.exp(-x)-x
plt.plot(x,y)
plt.grid(True)
plt.show()
