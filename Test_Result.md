# Отчёт о тестировании "Bank_bug"
## Проверка ошибки при пополнении счета
08.03.2020 - 08.03.2020 было проведено тестирование


На тестирование затрачено: 30 минут

В результате тестирования выявлен следующий дефект
+ Не корректное значение счета при выходе за границы размера типа переменной. Для хранения чисел более  2147483647 не подходит тип "int".

### Описание процесса тестирования
В ходе тестирования была создана аналогичная часть кода, в которой были использованы те же типы переменных
При сложении двух чисел 2_000_000_000 и 500_000_000 ожидается результат 2_500_000_000.
Так как тип int содержит в себе максимум 32 бита, данное значение выходит за границы. 
Получен другой результат "-1794967296".


Тестирование производилось в следующем окружении:
```
Windows 10 x64
Openjdk version "11.0.6" 2020-01-14
OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.6+10)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.6+10, mixed mode)
Intellj IDEA 2019.3.3
```