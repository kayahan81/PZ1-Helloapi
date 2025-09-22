---
# Практическое задание 1

## ЭФМО-02-25

## Алиев Каяхан Командар оглы
---
# Информация о проекте

Примитивный HTTP-сервер на языке Go с тремя эндпоинтами

# Цель практической работы
Цель : Развернуть рабочее окружение Go на Windows, создать минимальный HTTP-сервис на net/http, подключить и использовать внешнюю зависимость, собрать и проверить приложение

# Задания :
-    Установить Go и Git, проверить версии.
-    Инициализировать модуль Go в новом проекте.
-    Релизовать HTTP-сервер с маршрутами /hello (текст) и /user (JSON) и /health (задание со звёздочкой).
-	Подключить внешнюю библиотеку (генерация UUID) и использовать её в /user.
-	Запустить и проверить ответы curl/браузером.
-	Собрать бинарник .exe и подготовить README и отчёт.

# Функциональность
- curl http://localhost:<порт>/hello - возвращает текстовое приветствие
- curl http://localhost:<порт>/user - возвращает JSON с данными пользователя, включая UUID
- curl http://localhost:<порт>/health - возвращает текущее время в RFC3339

# Файловая структура проекта:

<img width="876" height="301" alt="структура проекта" src="https://github.com/user-attachments/assets/6f32dd3a-7065-41b9-8c60-cbae37d7cfb6" />

# Требования
Go: 1.25.1 или новее
Git: 2.51.0 или новее

<img width="841" height="232" alt="Установка Git и Go" src="https://github.com/user-attachments/assets/9f703675-a68b-484e-9e13-a80983a82620" />


# Команды запуска/сборки
Для запуска Helloapi нужно выполнить 4 шага:
## 1) Клонировать данный репозиторий в удобную для вас папку:
```Powershell
git clone https://github.com/kayahan81/PZ1-Helloapi
```
## 2) Перейти в папку helloapi:
```Powershell
cd helloapi
```
## 3) Загрузка зависимостей:
```Powershell
go mod tidy
```
## 4) Команда запуска
```Powershell
go run ./cmd/server
```

Порт по умолчанию будет 8080, допускается работа с другими портами (проверено с портов 8081)

## Команда сборки
Для сборки бинарника и запуска .exe файла используются данные программы

```Powershell
go build -o helloapi.exe ./cmd/server
.\helloapi.exe
```

Порт сервера можно изменить через переменную окружения APP_PORT(если её не использовать, то будет использоваться порт 8080)

Команда для PowerShell:
```Powershell
$env:APP_PORT="8081"
```

Результат после изменения:

<img width="996" height="81" alt="Запуск на другом порту" src="https://github.com/user-attachments/assets/fa4f8911-ed36-47c1-a3b9-8792ac060f5f" />

# Отчётные материалы

### Эндпоинт /hello

<img width="1431" height="596" alt="В другом окне PowerShell проверьте эндпоинты Hello" src="https://github.com/user-attachments/assets/69d39ffc-55f1-49dd-98c7-0d88bc4de2fd" />

### Эндпоинт /user

<img width="1392" height="560" alt="В другом окне PowerShell проверьте эндпоинты User" src="https://github.com/user-attachments/assets/fb9de5aa-990f-4a97-8ecb-53b793a28bd1" />

### Эндпоинт /health

<img width="1381" height="526" alt="Доп  звёздочка добавить health c JSON " src="https://github.com/user-attachments/assets/05365653-aba4-4a54-91fd-73560fc51868" />



