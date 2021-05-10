# Dichotomie-

import math as m

def Dichotomie(f, a0, b0, epsilon, Nitermax):
    an = a0
    bn = b0
    n = 1
    while abs(bn - an)> epsilon and n < Nitermax:
        m=(an + bn)/2
        if (f(an)*f(m) <= 0):
            bn = m
        else:
            an = m
        n+=1
    return m, n


def f1(x):
    return x**4+3*x-9
print("1:", Dichotomie(f1, 1.4, 2, 10**(-10), 100000))
print("1:", Dichotomie(f1, -1.5, -2, 10**(-10), 100000))

def f2(x):
    return x-3*m.cos(x)+2
print("2:",Dichotomie(f2, 0.5, 2, 10**(-10), 100000))
print("2:",Dichotomie(f2, -0.5, -2, 10**(-10), 100000))
print("2:",Dichotomie(f2, -4, -3, 10**(-10), 100000))

def f3(x):
    return x*m.exp(x)-7
print("3:",Dichotomie(f3, 1.5, 2, 10**(-10), 100000))


def f4(x):
    return m.exp(x) -x -10
print("4:",Dichotomie(f4, 2.5, 3, 10**(-10), 100000))
print("4:",Dichotomie(f4, -10, -9, 10**(-10), 100000))
#1
def f5(x):
    return 2*m.tan(x)-x-5
print("5:",Dichotomie(f5, 1, 2, 10**(-10), 100000))

def f6(x):
    return m.exp(x)- x**2 - 3
print("6:",Dichotomie(f6, 1.8, 2, 10**(-10), 100000))
#
def f7(x):
    return 3*x+4*m.log(x)-7
print("7:",Dichotomie(f7, 1.5, 2, 10**(-10), 100000))

#
def f8(x):
    return x**4 - 2*x**2 +4*x-17
print("8:",Dichotomie(f8, 2, 3, 10**(-10), 100000))
print("8:",Dichotomie(f8, -2.5, -3, 10**(-10), 100000))
#1
def f9(x):
    return m.exp(x)- 2*m.sin(x)- 7
print("9:",Dichotomie(f9, 2, 3, 10**(-10), 100000))

def f10(x):
    return (m.log(x**2 + 4))*(m.exp(x))- 10
print("10:",Dichotomie(f10, 1.5, 2, 10**(-10), 100000))


