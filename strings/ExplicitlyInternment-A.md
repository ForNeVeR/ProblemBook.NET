# «ExplicitlyInternment» (Решение)
```
True
True
False
True
```
Первые две строчки содержат `True`, т.к. для выражений `x == y` и `x == z` будет вызвана перегрузка оператора `==` для строк, а строки совпадают. В последних двух строчках будет вызвана перегрузка оператора `==` для объектов, которая сравнит объекты по ссылке. Строка `"AB"` является заинтернированной и хранится в специальной таблице памяти. Переменная `x` указывает на интернированное значение, т.к. определена с помощью литерала. Переменная `z` указывает на это же значение, т.к. определена с помощью метода `string.Intern`. А переменная `y` будет указывать на другую область памяти, т.к. была определена через `StringBuilder`, который при вызове метода `ToString()` не учитывает интернированные значения.
[Задача](./ExplicitlyInternment-Q.md)
