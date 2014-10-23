st = input()
j = 0
for i in range(len(st)):
    if st[i] == ' ':
        j = i
st1 = st[0:j]
n = int(st1)
st1 = st[(j+1):len(st)]
k = int(st1)

i = 0
a = []
st = input() + ' '
while i <= (len(st) - 1):
    j = i
    while (st[i] != ' '):
        i += 1
    a.append(int(st[j:i]))
    i += 1
  
cnt = 0
mm = 10000000
i_max = 0
i_min = 0
x = []
y = []
while cnt < k:
    if (max(a) - min(a)) >= mm:
        cnt -= 1
        del x[0]
        del y[0]
        break
    mm = max(a) - min(a)
    for i in range(len(a)):
        if a[i] == max(a):
            i_max = i
            for j in range(len(a)):
                if a[j] == min(a):
                    i_min = j
                    x.append(i_max)
                    y.append(i_min)
                    a[i_max] -= 1
                    a[i_min] += 1
                    cnt += 1

    
print((max(a) - min(a)), cnt)
x = x[::-1]
y = y[::-1]
for i in range(cnt):
    print((x[i]+1), (y[i]+1))
