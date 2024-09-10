# Практическое занятие №1. Введение, основы работы в командной строке


## Задача 1
```cut -d: -f1 /etc/passwd |sort```
![photo_2024-09-10_09-31-24](https://github.com/user-attachments/assets/7ef8ec46-2c0e-4434-9d43-de78ad401dd9)



## Задача 2
```cat /etc/protocols | awk '{print $2, $1}' | sort -rn | head -n 5 | awk '{printf "%d %s\n", $1, $2}'```
![photo_2024-09-10_09-31-24](https://github.com/user-attachments/assets/5a0d670e-d743-493a-b5a1-258ce42b6f7d)


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
![3quest](https://github.com/user-attachments/assets/2ee144b9-dd7c-480c-9bbf-c116a0061f31)


## Задача 4
```
grep -oE '\b[a-zA-Z_][a-zA-Z0-9_]*\b' hello.go | grep -vE '\b(int|void|return|if|else|for|while|include|stdio)\b' | sort | uniq
```
<img width="1108" alt="4quest" src="https://github.com/user-attachments/assets/28214792-f487-4d37-abc8-168e217e3d6e">
