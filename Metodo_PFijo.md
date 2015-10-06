import numpy as np
import matplotlib.pyplot as plt
val =0
n=0
cont=float(0)
g=float(0)

graf=[]
def f(x):
    val=((3+((x)**2))/(2))
    return val
def h(x):
    gr=x**2-2*x+3
    return gr
#n=input()
    
print "|%-7s|%-15s|%-11s|"%("Xi","PFijo","ErrA")
print "|%-7s|%-11s|%-11s|"%("-------","---------------","-----------")

while(n<10):
    g=(3+((cont)**2))/(2)
    err=((g-cont)/(g))*100
    fun=h(n)
    graf.append(fun)
    cont=g
    
    print "|%-7d|%-15e|%-10.5e|"%(n,g,err)
    n+=1
plt.plot(graf)
plt.show()

