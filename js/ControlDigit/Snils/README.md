### Контрольное число

Контрольное число, контрольная цифра — разновидность контрольной суммы, добавляется обычно в конец длинных номеров с целью первичной проверки их правильности. Применяется с целью уменьшения вероятности ошибки при обработке таких номеров: машинном считывании с упаковки товара, записи в документы, голосовой передаче от человека к человеку
Wikipedia

### Реализовать контрольное число для СНИЛС
Алгоритм формирования контрольного числа СНИЛС:

Контрольное число СНИЛС рассчитывается следующим образом:
1. Каждая цифра СНИЛС умножается на номер своей позиции (позиции отсчитываются с конца)
2. Полученные произведения суммируются
  2.1 Если сумма меньше 100, то контрольное число равно самой сумме
  2.2 Если сумма равна 100 или 101, то контрольное число равно 00
  2.3 Если сумма больше 101, то сумма делится по остатку на 101 и контрольное число определяется остатком от деления аналогично пунктам 2.1 и 2.2

Например: указан СНИЛС 112-233-445 95. Проверяем правильность контрольного числа:
цифры номера 1 1 2 2 3 3 4 4 5
номер позиции 9 8 7 6 5 4 3 2 1
Сумма = 1×9 + 1×8 + 2×7 + 2×6 + 3×5 + 3×4 + 4×3 + 4×2 + 5×1 = 95. Сумма равна контрольному числу. Контрольное число 95 — указано верно.


Реализуйте метод controlNumber(number), который принимает максимум девятизначное число, обозначающее СНИЛС, а вернет подсчитанное контрольное число ([0..99])