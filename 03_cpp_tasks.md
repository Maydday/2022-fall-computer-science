# Практика

## Разминка

1. Создайте в своём репозитории `2022-polytech-%фамилия%` пустой файл README.md в директории `03_cpp/intro`
2. Сделайте коммит
3. Напишите программу, которая запрашивает имя пользователя и выводит его обратно в строке "Hello, %имя пользователя%!"
4. Настройте cmake-проект 
5. Отправьте решение на GitHub

## Задание

### Калькулятор
1. Создайте в своём репозитории `2022-polytech-%фамилия%` пустой файл README.md в директории `03_cpp/calculator`
2. Настройте cmake-проект
3. Напишите программу, которая в бесконечном цикле считывает команды пользователя, вычисляет результат и выводит его (это [REPL-режим](https://ru.wikipedia.org/wiki/REPL))
4. Реализуйте опреации вида `a $ b`, где `a` и `b` — вещественные числа, а `$` — операции: `+`, `-`, `*`, `/`, `^` (возведение в целочисленную степень) 
5. Совет: разделите программу на несколько файлов
6. Отправьте решение на GitHub

## Домашнее задание
1. Создайте в своём репозитории директорию `03_cpp/gcd`
2. Возьмите заготовку (см. ниже) и напишите программу, которая вычисляет наибольший общий делитель двух целых чисел с помощью алгоритма Евклида (см. литературу)
3. В `main` выполняются проверочные запуски функции `gcd` с помощью `assert` (см. документацию). Обеспечьте корректное выполнение всех проверок

```cpp
#include <iostream>
#include <cassert>

int gcd(int a, int b) {

  if (a < 0) a *= -1;
  if (b < 0) b *= -1;

  // Решение тут

  return 0;
}

int main() {
  assert(gcd(0, 5) == 5);
  assert(gcd(9, 0) == 9);
  assert(gcd(48, 64) == 16);
  assert(gcd(-64, 48) == 16);
  assert(gcd(30, 18) == 6);
  assert(gcd(-30, -18) == 6);
  assert(gcd(270, 192) == 6);

  return 0;
}

```

*Комментарии*
- В этом файле есть опечатки, вы можете их исправить через pull request.
- Всю работу удобно вести в отдельной ветке и затем влить готовый результат в основную ветку.
- `gcd(a, 0) = |a|` для `a ≠ 0`, так как любое число является делителем 0, а наибольший делитель числа `a` это `|a|`.
