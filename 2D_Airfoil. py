import numpy as np

## Simpsons Rule

def Simpson(Y,a,b):
    n = len(Y)-1
    LB = Y[0]+Y[n]
    intx = (b-a)/(n)
    if n != 1:
        for i in range(1,n):
            if (i%2) == 0:
                LB += 2*Y[i]
            else:
                LB += 4*Y[i]
    
    return (intx/3) * LB
    
## Cl inputs
X_LE = 0; X_TE = 1 #Define the leading and trailing edge
C_pu = np.linspace(0,10,9) #Coefficient of pressure uper
C_pl = np.linspace(0,5,9) #Coefficient of pressure lower

C_l = (1/(X_TE-X_LE))*(Simpson(C_pl,X_LE,X_TE)-Simpson(C_pu,X_LE,X_TE))
print(C_l)

    
