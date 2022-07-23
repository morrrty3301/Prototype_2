# Prototype_2
def p(n):
    sn = str(n)
    Sn = sn[::-1]
    if sn == Sn and n > 9:
        return True
    else:
        return False

def f(n):
    d = 2
    a = []
    G = 0
    while d * d <= n:
        if n % d == 0:
            a.append(d)
            a.append(n//d)
        d += 1
    for i in range(len(a)):
        if p(a[i]):
            G += a[i]
    return G

           
maxg = 0
for i in range(100001):
    maxg = max(maxg, f(i))

print(maxg)
