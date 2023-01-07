# Home_Work_2.Py

1)'''
Напишите программу, которая принимает на вход вещественное число и показывает сумму его цифр.
Пример:
- 6782 -> 23
- 0,56 -> 11
'''

number = input('Введите число ')

def sum(number):                            
    if float(number) < 0:                            
        x = float(number) * (-1)
    help = 0

    for i in str(number):
        if i != '.':
            help += int(i)
    return help

   
print(f'Сумма чисел равна {sum(number)}')

2)'''
Напишите программу, которая принимает на вход число N и выдает набор произведений чисел от 1 до N.
Пример:
- пусть N = 4, тогда [ 1, 2, 6, 24 ] (1, 1*2, 1*2*3, 1*2*3*4)
'''

n = int(input('Введите число: '))
a = 1
for i in range(n):
    a *= i + 1
    print(a)
    
3)'''
Задайте список из n чисел последовательности (1+1/n)**n и выведите на экран их сумму.
'''

number = int(input('Введите число: '))
a = 1

for i in range(number):
    a = 1+1/number
    a = a ** number
    print(round(a,2))
    number -= 1
   
4)'''
Задайте список из N элементов, заполненных числами из промежутка [-N, N]. Найдите произведение элементов на указанных позициях. 
Позиции хранятся в отдельном списке( пример n=4, lst1=[4,-2,1,3] - списко на основе n, а позиции элементов lst2=[3,1].
'''

from random import randint
numbers = []
for i in range(10):
    numbers.append(randint (-10,10))
print(numbers)

def get_numbers(numbers):
    count =0 
    for element in numbers:
        count +=1
    return count
print('Номер элемента: ', get_numbers(numbers))

x = int(input('Введите позицию первого элемента: '))
y = int(input('Введите позиицю второго элемента: '))

for i in range(len(numbers)):
    mult = numbers[x -1]*numbers[y - 1]
print(f'Итог: {numbers[x -1]} * {numbers[y -1]} =', mult)

5)'''
Реализуйте алгоритм перемешивания списка. (рандомно поменять местами элементы списка между собой)
'''

from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
print(x)
