# Задача 2. 5 наибольших портов из `/etc/protocols`

## Задание

Вывести данные `/etc/protocols` в отформатированном и отсортированном порядке для 5 наибольших портов.

## Решение

```bash
awk '!/^#/ && NF {print $2, $1}' /etc/protocols | sort -rn | head -5
```

## Пример вывода

```text
142 rohc
141 wesp
140 shim6
139 hip
138 manet
```
