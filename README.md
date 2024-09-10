# Практическое занятие №1. Введение, основы работы в командной строке


## Задача 1
```cut -d: -f1 /etc/passwd |sort```


## Задача 2
```cat /etc/protocols | awk '{print $2, $1}' | sort -rn | head -n 5 | awk '{printf "%d %s\n", $1, $2}'```


## Задача 3
```
#!/bin/bash

if [ $# -eq 0 ]; then

    echo "Использование: $0 \"Ваш текст\""

    exit 1

fi


text="$1"


length=${#text}


border=$(printf "%0.s-" $(seq 1 $((length + 2))))

border="+$border+"


echo "$border"

echo "| $text |"

echo "$border"
```            


## Задача 4
```
grep -oE '\b[a-zA-Z_][a-zA-Z0-9_]*\b' hello.go | grep -vE '\b(int|void|return|if|else|for|while|include|stdio)\b' | sort | uniq
```
