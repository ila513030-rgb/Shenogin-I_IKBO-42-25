# Задание 2

Вывести пять протоколов с наибольшими номерами из `/etc/protocols`.

```bash
grep -v '^#' /etc/protocols | awk 'NF >= 2 {print $2, $1}' | sort -nr | head -5
```

Ожидаемый результат для используемого файла:

```text
142 rohc
141 wesp
140 shim6
139 hip
138 manet
```
