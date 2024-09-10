# Практическое занятие №1. Введение, основы работы в командной строке

## Задача 1


```cut -d: -f1 /etc/passwd |sort```

![image](https://github.com/user-attachments/assets/86289e2e-5fb0-4f73-8a89-5c7203476113)

## Задача 2

```cat /etc/protocols | awk '{print $2, $1}' | sort -rn | head -n 5 | awk '{printf "%d %s\n", $1, $2}'```

![image](https://github.com/user-attachments/assets/7d6c8609-88c2-4746-bb7b-a4b4898deab1)

## Задача 3

```
#!/bin/bash
# Проверяем, был ли передан аргумент

if [ $# -eq 0 ]; then

    echo "Использование: $0 \"Ваш текст\""

    exit 1

fi

# Получаем текст из аргумента

text="$1"

# Вычисляем длину текста

length=${#text}

# Создаем верхнюю и нижнюю границы

border=$(printf "%0.s-" $(seq 1 $((length + 2))))

border="+$border+"

# Выводим баннер

echo "$border"

echo "| $text |"

echo "$border"
```  
![image](https://github.com/user-attachments/assets/fcd7f1b3-0ff9-4910-b739-76a36a040c64)

## Задача 4
`grep -oE '\b[a-zA-Z_][a-zA-Z0-9_]*\b' hello.c | grep -vE '\b(int|void|return|if|else|for|while|include|stdio)\b' | sort | uniq`

![image](https://github.com/user-attachments/assets/e3a3eb6b-344b-4e4e-8609-ca0d06240e0e)

## Задача 5
```
chmod +x reg
./reg banner
```
![image](https://github.com/user-attachments/assets/1802518b-4209-47f1-abbf-f89920483688)

## Задача 7
```
chmod +x find_duplicates.sh
./find_duplicates.sh /Users/aslav/Documents/cdr
```
### code is presented in the file bash/find_duplicates.sh

![7quest.png](photos/7quest.png)

## Задача 8
```
go run archiver.go /Users/aslav/Documents/cdr  .log
```
### code is presented in the file code/archiver.go

![8quest.png](photos/8quest.png)

## Задача 9
```
cd code
go run replacer.go /Users/aslav/Desktop/RTU_MIREA_2COURCE/КонфигУправ/1Pract/trash/testFor8.txt testFor8output.txt

```
### code is presented in the file code/replacer.go

![9questTerminal.png](photos/9questTerminal.png)
![9questFile.png](photos/9questFile.png)

## Задача 10
```
cd code
go run dirReader.go /Users/aslav/Downloads 
```
### code is presented in the file code/dirReader.go

![10quest.png](photos/10quest.png)


