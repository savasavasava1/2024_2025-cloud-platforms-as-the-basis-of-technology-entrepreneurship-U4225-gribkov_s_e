### University: ITMO University
### Faculty: FTMI
### Course: Cloud platforms as the basis of technology entrepreneurship
### Year: 2024/2025
### Group: U4225
### Author: Gribkov Savelii Evgenievich
### Lab: Lab2
### Date of create: 04.11.2024
### Date of finished: tbc

# Лабораторная работа 2 - Исследование Cloud Run

## Цель работы: 
Ознакомиться с работой Cloud Run
## Ход работы:

1) Создал Cloud Run из представленного дефолтного сервиса Hello с минимальным количеством ресурсов
![image](https://github.com/user-attachments/assets/9e9c355b-1728-4e45-9b0c-886a184f2cda)
![image](https://github.com/user-attachments/assets/ed71dc69-127d-4759-9e63-b00e62fea3c6)
![image](https://github.com/user-attachments/assets/35c055ed-cb1a-4736-a75d-87f8131a2c4f)

Разберу информацию, полученную с лога:
![image](https://github.com/user-attachments/assets/3937f9f5-5027-4525-b270-2da16d573b15)
- Создан новый сервис в Cloud Run с именем "sgribkov-lab2"
- Запущен контейнер (сообщение Hello from Cloud Run!) + контейнер ожидает HTTP-запросов на порту 8080
- Начата обработка HTTP-запросов (метод GET) с клиента Chrome

2) Анализ метрик
Метрики показывают различные стандартные параметры сервиса, а именно: число запросов, задержка запросов, подсчет инстанций сервиса, сколько памяти использует сервиса и пр.
![image](https://github.com/user-attachments/assets/ae144c2c-f18c-49d2-aa5f-aec29c9724f9)
![image](https://github.com/user-attachments/assets/1f37e849-5d25-4d37-8b9c-3f4e24f45ea4)


3) Поменял порт на 8090
![image](https://github.com/user-attachments/assets/e4cedeb0-2f1c-4b46-879e-7ebc514db571)
Проверил по логам и метрикам - Контейнер снова успешно запустился, логи показывают операцию ReplaceService, то есть Cloud Run заменяет старый сервис на новый с обновленными конфигурациями (новый порт 8090)
![image](https://github.com/user-attachments/assets/547adf1b-7d29-4981-9ad9-b33649550e88)

4) Равномерно распределил трафик в пропорции 50/50 между двумя портами
![image](https://github.com/user-attachments/assets/7f91a240-7dba-4ff8-89cf-0d9056d35ccf)


7) Произвел очистку и удалил VM
