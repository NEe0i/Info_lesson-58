# Info_lesson-58
1. это многократное выполнение одинаковых действий
2. цикл с условием выпольняеться до тех пор когда условие не будет
3. это цикл в котором условие проверяеться в конце
4. Цикл с предусловием не выполняется ни разу, если изначально условие ложно
5. Программа может зациклиться, если условие окончания цикла никогда не становится истинным. Например: i := 0; while (i < 10) do begin
6. если переменная начального значения нарушает условия выполнения цикла
7. а, любой цикл с переменной можно заменить циклом с условием. Но обратное нельзя, так как у цикла с переменной фиксированное количество итераций, а у цикла с условием — нет
8. Если известно количество итераций заранее
9. Если программа ожидает положительное число, то при вводе отрицательного числа может работать неправильно или выдавать неверный результат. Нужно добавить обработку отрицательных чисел, например, преобразовать число в положительное


ЗАДАЧИ

1. a = int(input("Введите первое число: ")) b = int(input("Введите второе число: ")) product = 0 for _ in range(abs(b)): product += abs(a) if (a < 0) != (b < 0): product = -product print("Произведение:", product)
2. N = int(input("Введите натуральное число N: ")) sum_ = 0 i = 1 while i <= N: sum_ += i i += 1 print("Сумма от 1 до N (циклом с условием):", sum_) с переменной: N = int(input("Введите натуральное число N: ")) sum_ = 0 for i in range(1, N + 1): sum_ += i print("Сумма от 1 до N (циклом с переменной):", sum_)
3.  N = int(input("Введите натуральное число N: ")) for i in range(1, N + 1): if i % 2 == 0: print(i)
4.  a = int(input("Введите первое натуральное число: ")) b = int(input("Введите второе натуральное число: ")) for i in range(a, b + 1): print(f"{i}{i}={ii}")
5.  a = int(input("Введите первое натуральное число: ")) b = int(input("Введите второе натуральное число: ")) sum_of_squares = 0 for i in range(a, b + 1): sum_of_squares += i * i print("Сумма квадратов:", sum_of_squares)
6.  N = int(input("Введите количество случайных чисел: ")) for _ in range(N): print(random.randint(1, 100))
7.  for number in range(10000, 100000): if number % 133 == 125 and number % 134 == 111: print(number)
8.   N = int(input("Введите натуральное число N: ")) for number in range(1, N + 1): digits = [int(d) for d in str(number) if int(d) != 0]  if all(number % d == 0 for d in digits): print(number)
9.   for num in range(100, 10000): digits = [int(d) for d in str(num)] power = len(digits) if sum(d ** power for d in digits) == num: print(num)
10.   M = int(input("Введите натуральное число M: ")) for num in range(M + 1): if str(num ** 2).endswith(str(num)): print(num)
11.   number = input("Введите число: ") count_even = sum(1 for digit in number if int(digit) % 2 == 0) print("Количество чётных цифр:", count_even)
12.   number = input("Введите число: ") digit_sum = sum(int(digit) for digit in number) print("Сумма цифр:", digit_sum)
13.   number = input("Введите число: ") has_adjacent_duplicate = any(number[i] == number[i + 1] for i in range(len(number) - 1)) print("Содержит ли число две одинаковые цифры рядом:", has_adjacent_duplicate)
14.   number = input("Введите число: ") is_all_same = all(digit == number[0] for digit in number) print("Состоит ли число из одинаковых цифр:", is_all_same)
15.    number = input("Введите число: ") has_duplicate = len(set(number)) < len(number) print("Содержит ли число хотя бы две одинаковые цифры:", has_duplicate)
16. exponent = 10 while exponent >= 2: if exponent % 2 == 0: print(f"2^{exponent} = {2 ** exponent}") exponent -= 1      Используя цикл с переменной:      for exponent in range(10, 1, -1): if exponent % 2 == 0: print(f"2^{exponent} = {2 ** exponent}")
17. a = int(input("Введите первое число: ")) b = int(input("Введите второе число: ")) steps = 0  while b != 0: a, b = b, a - b steps += 1   print("НОД =", a) print("Количество шагов:", steps)
18. a = int(input("Введите  число: ")) b = int(input("Введите число: ")) steps = 0  while b != 0: a, b = b, a % b steps += 1   print("НОД =", a) print("Количество шагов:", steps)
19. a = 64168 b = 82678     Выполнение для первого метода steps1 = 0 while b != 0: a, b = b, a - b steps1 += 1  nod1 = a      Выполнение для второго метода a = 64168 b = 82678 steps2 = 0 while b != 0: a, b = b, a % b steps2 += 1    nod2 = a      print("НОД(a, b):", nod1) print("Шаги-1:", steps1) print("Шаги-2:", steps2)
20. sum_nums = 0 product = 1      for _ in range(10): number = int(input("Введите число: ")) sum_nums += number product *= number      print("Сумма:", sum_nums) print("Произведение:", product)
21. sum_nums = 0 product = 1 while True: number = int(input("Введите число (0 для выхода): ")) if number == 0: break sum_nums += number product *= number    print("Сумма:", sum_nums) print("Произведение:", product)
22. min_num = float('inf') max_num = float('-inf')    while True: number = int(input("Введите число (0 для выхода): ")) if number == 0: break if number < min_num: min_num = number if number > max_num: max_num = number    print("Минимальное число:", min_num)    print("Максимальное число:", max_num)
23. N = int(input("Введите натуральное число: ")) factorial = 1 for i in range(1, N + 1): factorial *= i    print("Факториал:", factorial
24. a = int(input("Введите натуральное число a: ")) N = int(input("Введите натуральное число N: ")) A = a ** N # это выражение может быть изменено, в зависимости от конкретного требования print("A =", A)
25. number = input("Введите число: ") for digit in number: print(digit)
26. N = int(input("Введите натуральное число N: ")) fib = [1, 1] while len(fib) < N: fib.append(fib[-1] + fib[-2]) print(f"Первые {N} чисел Фибоначчи: {fib[:N]}")
27. a = int(input("Введите число a: ")) b = int(input("Введите число b: "))def is_prime(n): if n < 2: return False for i in range(2, int(n**0.5) + 1): if n % i == 0: return False return True    primes = [num for num in range(a, b + 1) if is_prime(num)] print("Простые числа в диапазоне:", primes)
28. N = int(input("Введите натуральное число N: ")) sum_divisors = sum(i for i in range(1, N) if N % i == 0) is_perfect = sum_divisors == N print("Является ли N совершенным:", is_perfect)
29. N = int(input("Введите натуральное число N: "))      def is_perfect(num): return sum(i for i in range(1, num) if num % i == 0) == num perfect_numbers = [num for num in range(1, N + 1) if is_perfect(num)] print("Совершенные числа в диапазоне:", perfect_numbers)
30. for x in range(186 // 15 + 1): # Ящики по 15 кг for y in range(186 // 17 + 1): # Ящики по 17 кг for z in range(186 // 21 + 1): # Ящики по 21 кг if 15 * x + 17 * y + 21 * z == 185: print(f"15*{x} + 17*{y} + 21*{z}") count += 1 print("Количество способов:", count)
31. result += str(digit)

if remainder == 0:
    return result  # если деление закончилось, возвращаем результат

if remainder in seen_remainders:
    period_start = seen_remainders[remainder]
    non_period = result[:period_start]
    period = result[period_start:]

  return f"{non_period}({period})"

seen_remainders[remainder] = len(result)  # фиксируем место начала текущего остатка
numerator = remainder
32.# Ведущий открывает пустой ящик, который не выбран участником и не содержит приз (только если есть возможность)
empty_box = next(box for box in range(3) if box != player_choice and box != prize_box)


new_choice = next(box for box in range(3) if box != player_choice and box != empty_box)


if player_choice == prize_box:
    stay_wins += 1
if new_choice == prize_box:
    switch_wins += 1
