# Лабораторная работа №1.2
## Цели: 
1. Изучить основные управляющие конструкции языка Python: условный
оператор и циклы.
2. Научиться использовать управляющие структуры для решения задач
различной сложности.
3. Закрепить навыки обработки данных с использованием коллекций и
итераторов.
4. Развить умение комбинировать условия и циклы для оптимизации
алгоритмов

## Задачи:
1. Освоить условный оператор if-elif-else и научиться применять его для
решения задач с разветвлением логики.
2. Понять работу циклов while и for, включая их особенности.
3. Изучить методы работы с коллекциями в циклах (например, списки, словари,
множества).
4. Разобраться с командами управления циклами break и continue.
5. Изучить коллекционные включения (list comprehensions) для создания новых
коллекций.
6. Практически применять комбинации условий и циклов для построения
сложных алгоритмов.
### 1. Рассчитать значение f при заданном значении вещественного числа x. При выводе на экран оставьте 2 знака после запятой
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

x = int(input("x = "))

if x >= 0:
    f = round(x**0.5 + x**2, 2)
else:
    f = round(1 / x, 2)

print("f =", f)
```
<img width="839" height="63" alt="image" src="https://github.com/user-attachments/assets/08d3199b-c928-46ab-ad41-a3496f0d9f81" />

### 2. Определите максимальное и минимальное значения из двух различных целых чисел.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231
# E-mail: PanshinaZA433@mgpu.ru

a1 = int(input("Введите целое число а1: "))
a2 = int(input("Введите целое число а2: "))

if a1 < a2:
  a_min = a1
  a_max = a2
  print(f"Максимум: {a_max}, минимум: {a_min}")
else:
  a_min = a2
  a_max = a1
  print(f"Максимум: {a_max}, минимум: {a_min}")
```
<img width="770" height="76" alt="image" src="https://github.com/user-attachments/assets/ea06a395-ca12-441f-b799-f4456127746c" />

### 3. Вася пытается высунуть голову в форточку размерами a и b см. Приняв условно, что его голова - круглая диаметром d см, определите, сможет ли Вася сделать это. Для прохождения головы в форточку необходим зазор в 1 см. с каждой стороны. Все величины - целые числа
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

a = int(input("Ширина форточки: "))
b = int(input("Высота форточки: "))
d = int(input("Диаметр головы: "))

if a > 0 and b > 0 and d > 0:
    fix = 1
    if d <= a-fix and d <= b-fix:
      print("Да")
    else:
      print("Нет")   
else:
    print("Проверьте ввод")
```
<img width="711" height="97" alt="image" src="https://github.com/user-attachments/assets/bbe87553-e1bc-4b10-b6c9-9fa2508dd196" />

### 4. Известны год и номер месяца сегодняшнего дня, а также год и номер месяца рождения человека (нумерация месяцев с 1: январь - 1 и т.д.). Определите возраст человека (число полных лет).
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

year_today = int(input("Введите текущий год: "))
month_today = int(input("Введите текущий месяц: "))

year = int(input("Введите год рождения: "))
month = int(input("Введите месяц рождения: "))

# Считается, введенные значения находятся в допустимых пределах,и
# что 'month_today' >= 'month' (проверять значения не нужно)
# Результат необходимо записать в переменную 'age'

if month_today >= month:
  age = year_today - year
else:
  age = year_today - year - 1

print("Число полных лет: ", age)
```
<img width="788" height="119" alt="image" src="https://github.com/user-attachments/assets/9b13117b-6331-4fc4-b773-96802b5e022d" />

### 5. Дана точка с целыми ненулевыми координатами (x;y). Определить номер четверти координатной плоскости, которой она принадлежит.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

x = int(input("Введите координту x: "))
y = int(input("Введите координту y: "))

if x > 0 and y > 0:
    print("1-я четверть")
elif x < 0 and y > 0:
    print("2-я четверть")
elif x < 0 and y < 0:
    print("3-я четверть")
else:
    print("4-я четверть")
```
<img width="764" height="77" alt="image" src="https://github.com/user-attachments/assets/6b7d6fe6-f1c0-4fd5-99c4-4c1549704c2b" />

### 6. Даны вещественные числа a, b, c (a≠0). Решите уравнение ax2+bx+c=0. При выводе значений оставьте 1 знак после запятой.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

a = int(input("a = "))
b = int(input("b = "))
c = int(input("c = "))

# Расчет дискриминанта
d = ((b**2) - (4*a*c))

if d > 0:
  x1 = round(((-b - (d**(1/2)))/(2*a)), 1)
  x2 = round(((-b + (d**(1/2)))/(2*a)), 1)
  print(f"x1 = {x1}, x2 = {x2}")
elif d == 0:
  x = round((-b/(2*a)), 1)
  print("x =", x)
else:
  print("Решений нет")
```
<img width="757" height="96" alt="image" src="https://github.com/user-attachments/assets/07f1724b-067f-48ce-824d-84430846c6e0" />

### 7. Дана непустая последовательность целых чисел, оканчивающаяся нулем. Найти сумму и количество введенных чисел.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

nums_sum = 0  # сумма
nums_count = 0  # количество

n = 1
x = int(input(f"Введите {n}-е число: "))
while x != 0:
    nums_sum = nums_sum + x
    nums_count += 1
    n += 1
    x = int(input(f"Введите {n}-е число: "))
print("Сумма =", nums_sum)
print("Количество =", nums_count)
```
<img width="788" height="74" alt="image" src="https://github.com/user-attachments/assets/b32bf61f-1f86-45ee-abe2-f01619ac4525" />

### 8. Дано число n. Из чисел 0,5,10,15,20,25,... напечатать те, которые не превышают n.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))
c = 0
while n >= c:
  print(c)
  c = c + 5
```
<img width="752" height="97" alt="image" src="https://github.com/user-attachments/assets/9dce73e5-ca65-4296-a308-d550cbcc3c83" />

### 9. Дано вещественное число a. Найдите наименьшее натуральное n, для которого верно неравенство
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

a = float(input("a = "))

n = 1
x_sum = 0
while x_sum <= a:
    x_sum += 1 / n
    n += 1

print(n - 1)
```
<img width="623" height="56" alt="image" src="https://github.com/user-attachments/assets/daea31ed-891f-4cec-b54b-1da5469c0a45" />

### 10. Дано натуральное число. Определите сумму и количество его цифр.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231
# E-mail: PanshinaZA433@mgpu.ru

n = int(input("n = "))

n_sum = 0
n_count = 0

while n > 0:
  n_sum = n_sum + n % 10
  n = n // 10
  n_count += 1

print("Сумма =", n_sum)
print("Количество =", n_count)
```
<img width="663" height="80" alt="image" src="https://github.com/user-attachments/assets/0369f295-b161-4fcb-96a8-8c1c00f6ba52" />

### 11. Вывести в строку 10 первых натуральных чисел, оканчивающихся на цифру k, кратных числу s и находящихся в интервале, левая граница которого равна start.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

start = int(input("start = "))
k = int(input("k = "))
s = int(input("s = "))
n_count = 10

res = []
x = start
while n_count != 0:
  if x % 10 == k and x % s == 0:
    res.append(str(x))
    n_count = n_count - 1
  x += 1 
print(" ".join(res))
```
<img width="764" height="109" alt="image" src="https://github.com/user-attachments/assets/261492f7-1b0c-460a-8abc-0ddd28d99b11" />

### 12. Даны целые числа a и b (a может быть больше b). Напечатайте: числа от минимального до максимального в строчку (разделяя пробелом); числа от максимального до минимального «столбиком».
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

a = int(input("a = "))
b = int(input("b = "))

if a > b:
  max = a
  min = b
  for i in range(a-b+1):
    print(b + i, end=" ")
  else:
    print(" ", sep='/n')
  for i in range(a-b+1):
    print(a - i)
else:
  max = b
  min = a
  for i in range(b-a+1):
    print(a + i, end=" ")
  else:
    print(" ", sep='/n')
  for i in range(b-a+1):
    print(b - i)
```
<img width="767" height="185" alt="image" src="https://github.com/user-attachments/assets/57c591cd-2b87-4582-bc2f-b5871405ed67" />

### 13. Для введенных с клавиатуры положительных целых чисел a и b (a≤b) определите: сумму всех целых чисел от a до b; произведение всех целых чисел от a до b; среднее арифметическое всех целых чисел от a до b; среднее геометрическое нечетных чисел от a до b. Отрезок поиска включает сами числа a и b. При выводе вещественных результатов оставьте два знака после запятой.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231
# E-mail: PanshinaZA433@mgpu.ru

a = int(input("a = "))
b = int(input("b = "))

n_sum = 0
n_mult = 1
n_avg = 0 
n_avg_geom = 0

count_n = 0
pr_n = 1

for i in range(b-a+1):
  n = a + i
  n_sum = n_sum + n
  n_mult = n_mult * n
  if n % 2 == 1:
    count_n = count_n + 1
    pr_n = pr_n * n

n_avg = round((n_sum/(b-a+1)), 2)  
if count_n > 0:
  n_avg_geom = round(pr_n ** (1 / count_n), 2)
else:
  n_avg_geom = 0

print("Сумма =", n_sum)
print("Произведение =", n_mult)
print(f"Среднее арифметическое = {n_avg}")
print(f"Среднее геометрическое нечетных чисел = {n_avg_geom}")
```
<img width="733" height="146" alt="image" src="https://github.com/user-attachments/assets/d9addae3-d0e4-4e15-a352-dcfed375a9b0" />

### 14. Начав тренировки, лыжник в первый день пробежал s км. (s>0, вещественное число). Каждый следующий день он увеличивал пробег на p % (0<p≤100, вещественное число) от пробега предыдущего дня. Определите: пробег лыжника за второй, третий, …, десятый день тренировок; какой суммарный путь он пробежал за первые 10 дней тренировок. При выводе вещественных результатов оставьте один знак после запятой.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = 1
s = float(input(f"Пробег за {n}-й день (км.) = "))
p = float(input("На сколько увеличивает пробег (%) = "))

total = s
while n < 10:
  s *= (p / 100) + 1
  total = total + s
  n += 1
  print(f"Пробег за {n}-й день: {round(s,1)} км.")

print(f"Суммарный пробег: {round(total, 1)} км.")
```
<img width="927" height="268" alt="image" src="https://github.com/user-attachments/assets/24f72693-0921-466e-9d99-a7a51eaf46dd" />

### 15. Известна масса каждого предмета в кг., загружаемого в грузовик. Определить, возможна ли перевозка груза, если грузоподъемность грузовика равна p кг
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

p = float(input("Грузоподъемность грузовика (кг.) = "))
n = int(input("Количество предметов = "))

total = 0
a = 1
for i in range(n):
  m = float(input(f"Масса {a}-го предмета (кг.) = "))
  total = total + m
  a += 1
if total <= p:
  print("Да")
else:
  print("Нет")
```
<img width="755" height="117" alt="image" src="https://github.com/user-attachments/assets/aa67d28e-70fc-4197-a9c2-69fcd681af59" />

### 16. В области несколько районов. Заданы площади, засеваемые пшеницей (га.), и средняя урожайность (ц/га) в каждом районе. Определите количество пшеницы, собранное по области. При выводе вещественных результатов оставьте один знак после запятой.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("Количество районов = "))

total = 0
a = 1
for i in range(n):
  s = int(input(f"Площадь {a}-го района (га) = "))
  y = int(input(f"Урожайность в {a}-м районе (ц/га.) = "))
  a += 1
  total = round((total + (s * y)), 1)
print(f"Собрано пшеницы: {total} ц.")
```
<img width="814" height="188" alt="image" src="https://github.com/user-attachments/assets/4b19c884-f9e8-48b0-932a-4014556786f8" />

### 17. Решите задачу № 7, организовав бесконечный цикл, который бы прерывался при выполнении условия, используя оператор break.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

nums_sum = 0  # сумма
nums_count = 0  # количество
i = 0
while True:
    x = int(input(f"Введите {i+1}-е число: "))
    if x == 0:
      break
    nums_sum = nums_sum + x
    nums_count += 1
    i += 1
print("Сумма =", nums_sum)
print("Количество =", nums_count)  
```
<img width="684" height="166" alt="image" src="https://github.com/user-attachments/assets/ff48cc74-11dc-419a-83eb-72e3aa7e0b6a" />

### 18. Предложение, введенное с клавиатуры, содержит слова из гласных и согласных букв кириллицы (регистр может быть различный), а также пробелы. Определите количество гласных и согласных букв в предложении. Для пропуска пробелов используйте оператор continue.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

sentence = str(input("Введите предложение: "))

count_gl = 0  # Кол-во гласных
count_sogl = 0  # Кол-во согласных

gl = "АаУуЫыЕеЁёОоИиЭэЮюЯя"

for c in sentence:
  if c == ' ':
    continue
  if c in gl:
    count_gl += 1
  else:
    count_sogl += 1
print(f"Кол-во букв в предложении: гласных - {count_gl}, согласных - {count_sogl}")
```
<img width="838" height="50" alt="image" src="https://github.com/user-attachments/assets/c310fe40-6ac9-4bd4-a5bb-89370a20d325" />

### 19. Выведите на экран (в строку) все целые числа от a до b, кратные некоторому числу c
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

a = int(input("a = "))
b = int(input("b = "))
c = int(input("c = "))

while a <= b:
  a = a + 1
  if a % c == 0:
    print(a, end=" ")
```
<img width="653" height="108" alt="image" src="https://github.com/user-attachments/assets/491c11bd-7a0e-4c2b-8183-ee1af96c7a60" />

### 20. Выведите на экран (в строку) все трехзначные натуральные числа, сумма цифр которых равна целому числу n (0<n≤27)
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))

res = []
x = 100
while x < 1000:
  if (x%10) + ((x//10)%10) + (x//100) == n:
    res.append(str(x))
  x += 1 
print(" ".join(res))
```
<img width="631" height="55" alt="image" src="https://github.com/user-attachments/assets/69015c55-5f8d-4a63-ad16-5b6605886876" />

### 21. Известно количество учеников в классе и их рост (см.); рост мальчиков условно задан отрицательными числами. Определите средний рост мальчиков и средний рост девочек. При выводе вещественных результатов оставьте один знак после запятой.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))

r_sr_m = 0.0
r_sr_d = 0.0
count_m = 0
count_d  = 0
sum_m = 0
sum_d = 0

for i in range(n):
  x = float(input(f"Рост {i+1}-го ученика = "))
  if x < 0:
    sum_m = sum_m + x
    count_m += 1
    r_sr_m = abs(round((sum_m / count_m), 1))
  else:
    sum_d = sum_d + x
    count_d += 1
    r_sr_d = round((sum_d / count_d), 1)

print(f"Средний рост мальчиков: {r_sr_m}")
print(f"Средний рост девочек: {r_sr_d}")
```
<img width="876" height="183" alt="image" src="https://github.com/user-attachments/assets/ce9a84d9-f794-49d7-ba48-88661d963424" />

### 22. Даны n вещественных чисел. Определите максимальное и минимальное из них. При выводе вещественных результатов оставьте два знака после запятой.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231
# E-mail: PanshinaZA433@mgpu.ru

n = int(input("n = "))

a_max = None
a_min = None

for i in range(n):
  x = float(input(f"{i+1}-е число = "))
  if a_max is None:
    a_max = round(x, 2)
    a_min = round(x, 2)
  else:
    if x > a_max:
      a_max = round(x, 2)
    if x < a_min:
      a_min = round(x, 2)

print(f"Максимум: {a_max}")
print(f"Минимум: {a_min}")
```
<img width="749" height="149" alt="image" src="https://github.com/user-attachments/assets/c10d557c-1442-47c5-b77a-ce794bcd5038" />

### 23. Дано натуральное число n. Определите, является ли оно членом последовательности Фибоначчи.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))

a, b = 0, 1
while b < n:
  a, b = b, a + b
print("Является" if b == n or n == 0 else "Не является")
```
<img width="635" height="52" alt="image" src="https://github.com/user-attachments/assets/b6321f40-1ec7-4393-abc4-3d9fcd99db22" />

### 24. Дано n вещественных чисел. Определите, является ли последовательность упорядоченной по возрастанию. В случае отрицательного ответа выведите порядковый номер числа, нарушающего такую упорядоченность.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))

# -1 означает, что последовательность упорядочена по возрастанию
# Если это не так, 'index' меняется в цикле на индекс элемента,
# нарушающего порядок
index = -1

prev = float(input("1-е число = "))
for i in range(n-1):
  a = float(input(f"{i+2}-е число = "))
  if a <= prev:
    index = i+2
    print(index)
    break
  prev = a
else:
    print("Является")
```
<img width="712" height="94" alt="image" src="https://github.com/user-attachments/assets/eb9edb2e-5b47-475b-81d3-b8387444c2f5" />

### 25. Выведите на экран таблицу умножения на n (2<n≤9)
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))

for i in range(1, n + 1):
    row = []
    for j in range(1, n + 1):
        row.append(f"{i} * {j} = {i * j:>2}")
    print("  ".join(row))
```
<img width="953" height="139" alt="image" src="https://github.com/user-attachments/assets/3b477d6c-f613-4151-9052-52004e5a824d" />

### 26. Выведите графическое изображения делимости чисел от 1 до n (значение n вводится с клавиатуры) - в каждой строке напечатайте очередное число и столько символов * , сколько делителей у этого числа.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))

for i in range(1, n + 1):
    count_d = 0
    for d in range(1, i + 1):
      if i % d == 0:
        count_d = count_d + 1
    print(i, "*" * count_d)
```
<img width="861" height="247" alt="image" src="https://github.com/user-attachments/assets/a3bc0e54-7669-452e-a70a-06673baa7ff0" />

### 27. Выведите на экран (в строку) n первых простых чисел
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))

f = 0
x = 2
pr =[]

while f < n:
  for d in range(2, x):
    if x % d == 0:
      break
  else:
    pr.append(str(x))
    f = f + 1 
  x = x + 1
print(" ".join(pr))
```
<img width="805" height="55" alt="image" src="https://github.com/user-attachments/assets/38ff6694-0809-4851-940b-49f48801056e" />

### 28. Составьте программу для нахождения всех натуральных решений уравнения x2+y2+z2=k2, где x,y,z∈[1,30], а k вводится с клавиатуры
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

k = int(input("k = "))

for x in range(1, 31):
    for y in range(1, 31):
        for z in range(1, 31):
            if x*x + y*y + z*z == k*k:
                print(f"x = {x}, y = {y}, z = {z}")
```
<img width="1051" height="355" alt="image" src="https://github.com/user-attachments/assets/95520a33-3b2f-4ca4-b75e-1e3b0650d96e" />

### 29. Дан список из n вещественных чисел, введенных с клавиатуры (среди чисел есть по крайней мере одно положительное и отрицательное число). Сформируйте из него 2 списка: положительных чисел, используя списковые включения; отрицательных чисел, не используя списковые включения. Выведите на экран: исходный список; получившиеся списки; среднее арифметическое первого списка и среднее геометрическое второго списка. При выводе вещественных результатов оставьте два знака после запятой
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("n = "))

nums = []
for i in range(n):
    x = float(input(f"Введите {i+1}-й элемент списка: "))
    nums.append(x)

nums_pos = [x for x in nums if x > 0]
nums_neg = []
for x in nums:
    if x < 0:
        nums_neg.append(x)

sr_ar = round((sum(nums_pos) / len(nums_pos)), 2)
pr = 1
for x in nums_neg:
    pr *= x
sr_geom = round((pr ** (1 / len(nums_neg))), 2)

print("Исходный список:", nums)
print("Положительные числа:", nums_pos)
print("Отрицательные числа:", nums_neg)
print("Ср. арифм.:", sr_ar)
print("Ср. геом.:", sr_geom)
```
<img width="934" height="220" alt="image" src="https://github.com/user-attachments/assets/7ba19d52-c6e8-4666-9ade-801a840f1437" />

### 30. Дан список целых чисел, введенных с клавиатуры (длина неизвестна). Ответьте на вопросы: являются ли все элементы положительными числами? есть ли хотя бы один нулевой элемент в списке? являются ли все элементы четными числами? есть ли хотя бы один нечетный элемент в списке? Каждый из пунктов выполните дважды: используя стандартный проход в цикле(например, через алгоритм с флажком), и используя функции any() и/или all().
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

# Все разделенные пробелом элементы будут преобразованы в список целых чисел
nums = [int(item) for item in input().split()]

# 1. Все положительные
for item in nums:
    if item <= 0:
        all_pos_1 = False
        break
else:
    all_pos_1 = True

all_pos_2 = all([item > 0 for item in nums])

# 2. Хотя бы 1 нулевой элемент
for item in nums:
    if item == 0:
        any_zero_1 = True
        break
else:
    any_zero_1 = False

any_zero_2 = any([item == 0 for item in nums])

# 3. Все четные
for item in nums:
    if item % 2 != 0:
        all_even_1 = False
        break
else:
    all_even_1 = True

all_even_2 = all(item % 2 == 0 for item in nums)

# 4. Хотя бы 1 нечетный элемент
for item in nums:
    if item % 2 != 0:
        any_odd_1 = True
        break
else:
    any_odd_1 = False

any_odd_2 = any(item % 2 != 0 for item in nums)

print("Все положительные:", all_pos_1, all_pos_2)
print("Хотя бы 1 нулевой элемент:", any_zero_1, any_zero_2)
print("Все четные:", all_even_1, all_even_2)
print("Хотя бы 1 нечетный элемент:", any_odd_1, any_odd_2)
```
<img width="897" height="126" alt="image" src="https://github.com/user-attachments/assets/ba43961e-7463-4993-8261-9552007cd996" />

### 31. Дано предложение. Выведите его на экран, удалив из него все слова, содержащие произвольную букву (вводится с клавиатуры).
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

s = input("Введите предложение = ")
k = input("Введите букву = ")

words = s.split()

f_words = []
for word in words:
  if k.lower() not in word.lower():
    f_words.append(word)
res = ' '.join(f_words)
print(res)
```
<img width="805" height="76" alt="image" src="https://github.com/user-attachments/assets/be43b2b1-5221-4bd4-af12-b5b711b324d3" />

### 32. В зрительном зале кинотеатра n рядов, количество мест в которых может меняться. Разработчик смоделировал занятость мест как двумерный массив (список из списков), где каждый вложенный список содержит информацию о проданных местах в соответствующем ряду (1 - занято, 0 - свободно). Напишите программу, которая позволит пользователю увидеть количество свободных мест, а также, введя номер ряда и места, получить информацию - свободно оно или нет. Данные о занятости мест вводятся с клавиатуры (набор из 0 и 1 для каждого ряда).
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

n = int(input("Количество рядов = "))

# 1. Заполнение мест
seats = []
for i in range(n):
    row = [int(x) for x in input().split()]
    seats.append(row)

# 2. Всего свободных мест
count = 0
for row in seats:
    for seat in row:
        if seat == 0:
            count += 1
print("Всего свободных мест:", count)

# 3. Ввод значений для поиска
#    Учитывайте, что пользователь привык считать с 1, а не с 0,
#    поэтому введенные сообщения необходимо скорректировать
n_p, m_p = [int(item) for item in
            input("Введите ряд и место через пробел: ").split()]

if n_p < 1 or n_p > n:
    print("Такого места не существует")
elif m_p < 1 or m_p > len(seats[n_p - 1]):
    print("Такого места не существует")
else:
    is_free = seats[n_p - 1][m_p - 1] == 0
    print(f"Место свободно: {is_free}")
```
<img width="1029" height="159" alt="image" src="https://github.com/user-attachments/assets/194e9a96-cef7-4377-9d7d-cfe1da8ed6db" />

### 33. Вводится список из n сотрудников, где все значения разделены пробелом и сами не содержат пробелов; Пол : "М" или "Ж" ; Стаж : количество полных лет, отработанных в компании. Сохраните введенные задания в виде списка списков, далее определите самого «молодого» и самого «старого» сотрудника, используя функцию sorted(); сформируйте 2 отельных списка: мужчин и женщин и ответьте, в каком из списков больше имен, начинающихся на букву k (вводится с клавиатуры)
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

# 1. Заполнение списка

# Используйте данный список для собственных тестов,
# чтобы избежать постоянного ввода значений
# Перед автоматической проверкой удалите/закомментируйте его
# и используйте ввод с клавиатуры
#employees = [
#    ["Петрова", "Анна", "Алексеевна", "Ж", 5],
#    ["Семенов", "Николай", "Михайлович", "М", 2],
#    ["Михайлов", "Игорь", "Васильевич", "М", 3]
#]

n = int(input("Количество сотрудников = "))

employees = []
for i in range(n):
    line = input().split()
    line[4] = int(line[4])
    employees.append(line)

# 2. Cамый «молодой» и самый «старый» сотрудник
sorted_employees = sorted(employees, key=lambda x: x[4])
employee_min = sorted_employees[0]
employee_max = sorted_employees[-1]
print("Cамый \"молодой\": {}".format(" ".join(employee_min[:3])))
print("Cамый \"старый\": {}".format(" ".join(employee_max[:3])))

# 3. Отдельные списки мужчин и женщин
#    В данном случае удобно использовать списковые включения
men = [emp for emp in employees if emp[3] == "М"]
women = [emp for emp in employees if emp[3] == "Ж"]

k = input("Введите букву начала имени = ").upper()

men_k_count = 0
for emp in men:
    if emp[1].startswith(k):
        men_k_count += 1

women_k_count = 0
for emp in women:
    if emp[1].startswith(k):
        women_k_count += 1

if men_k_count > women_k_count:
    print("У мужчин таких имен больше")
elif women_k_count > men_k_count:
    print("У женщин таких имен больше")
else:
    print("Таких имен поровну у мужчин и женщин")
```
<img width="1149" height="183" alt="image" src="https://github.com/user-attachments/assets/042fea65-3514-4f20-a139-f6cd300a08b0" />

### 34. Вводится список из n годовых вкладов, предлагаемых банками, где все значения разделены пробелом и сами не содержат пробелов; наименование банка уникально; Сумма : сумма для открытия вклада в руб. (целое число, >0); Процент : годовой процент по вкладу (вещественное число, (0,100]). Сохраните введенные данные в виде списка словарей. Далее определите (гарантируется, что искомый банк - один): самый доступный банк (с наименьшей первоначальной суммой); самый выгодный банк, принимая, что за год прибыль = сумма * процент / 100. При выводе финансовых значений оставьте два знака после запятой.
```
# Выполнила: Паньшина З.А.
# Группа: АБП-231

# 1. Заполнение списка

# Используйте данный список для собственных тестов,
# чтобы избежать постоянного ввода значений
# Перед автоматической проверкой удалите его
# и используйте ввод с клавиатуры
# deposits = [
#    {"name": "Банк_1", "initial_sum": 50000, "rate": 5.2},
#    {"name": "Банк_2", "initial_sum": 20000, "rate": 3.7},
#    {"name": "Банк_3", "initial_sum": 45000, "rate": 6.8},
# ]

n = int(input("Количество банков = "))

deposits = []
for i in range(n):
    line = input().split()
    name = line[0]
    initial_sum = int(line[1])
    rate = float(line[2])
    deposits.append({
        "name": name,
        "initial_sum": initial_sum,
        "rate": rate
    })

# 2. Самый доступный банк (с наименьшей первоначальной суммой)
min_deposit = min(deposits, key=lambda x: x["initial_sum"])
print(f"Самый доступный банк: {min_deposit['name']}, первоначальная сумма: {min_deposit['initial_sum']:.2f} руб.")

# 3. Самый выгодный банк
#    прибыль = сумма * процент / 100

max_prib = 0
best_bank = None
for deposit in deposits:
    prib = deposit["initial_sum"] * deposit["rate"] / 100
    if prib > max_prib:
        max_prib = prib
        best_bank = deposit

print(f"Самый выгодный банк: {best_bank['name']}, прибыль: {max_prib:.2f} руб.")
```
<img width="937" height="143" alt="image" src="https://github.com/user-attachments/assets/2b6ea05f-e90c-4ea7-8ff3-95aee894ae69" />

## Вывод:
В ходе выполнения лабораторной работы изучены основные управляющие конструкции языка python, методы работы с коллекциями в циклах, развито умение комбинировать условия и циклы для оптимизации алгоритмов, а также закреплены навыки обработки данных с использованием коллекций и иттераторов.
