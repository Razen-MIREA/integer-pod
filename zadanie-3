num = -37
k = 8

def sbit(x,m):
    return bin(int(x,2)+m)[2:].zfill(k-1)

def pod(num, k):
    # знак
    z = '0' if num>0 else '1'; z+=','
    # прямой
    b = str(bin(num))
    b = b[2:] if num>0 else b[3:]
    b = b.zfill(k-1)
    # обратный
    b1 = ''.join(['0' if int(x) else '1' for x in b])
    # дополнительный
    b2 = sbit(b1,1) if num<0 else b1
    return(z,b,b1,b2)
z,b,b1,b2 = pod(num, k)

# вывод
print(f'Перевод числа {num} в 8-битный код:\n')
print(f'Прямой код: {z+str(b)}')
print(f'Обратный код: {z+str(b1)}')
print(f'Дополнительный код: {z+str(b2)}')
print('-'*30)
print('(✓-Все хорошо / ✗-Переполнение)\n')

p = '✓' if -128<int(b,2)+90<128 else '✗'
print(f'Прямой код: {z+str(b)}')
print(f'{num} + 90 = {num+90}, {z+str(b)} + {pod(90,8)[0]+pod(90,8)[1]} = {pod(90+num,8)[0]+pod(90+num,8)[1]} ({p})')
print('')
p1 = '✓' if -128<int(b1,2)+90<128 else '✗'
print(f'Обратный код: {z+str(b1)}')
print(f'{int(b1,2)} + 90 = {int(b1,2)+90}, {z+str(b1)} + {pod(90,8)[0]+pod(90,8)[1]} = {pod(90+int(b1,2),8)[0]+pod(90+int(b1,2),8)[1]} ({p1})')
print('')
p2 = '✓' if -128<int(b2,2)+90<128 else '✗'
print(f'Дополнительный код: {z+str(b2)}')
print(f'{int(b2,2)} + 90 = {int(b2,2)+90}, {z+str(b2)} + {pod(90,8)[0]+pod(90,8)[1]} = {pod(90+int(b2,2),8)[0]+pod(90+int(b2,2),8)[1]} ({p2})')
