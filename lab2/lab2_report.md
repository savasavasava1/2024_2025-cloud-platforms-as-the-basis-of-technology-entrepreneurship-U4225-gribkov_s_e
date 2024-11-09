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
![image](https://github.com/user-attachments/assets/4e87b2ac-4d1e-4a21-8912-3374bae639ac)
![image](https://github.com/user-attachments/assets/07a76625-b74c-44ac-a8dd-a271dc525e95)
![image](https://github.com/user-attachments/assets/49eb7f70-5bb1-4777-aa89-3d516299dbb2)


3) Поменял порт на 8090
![image](https://github.com/user-attachments/assets/c4cbb032-b29c-4ea9-8288-de22bf167c41)


7) Произвел очистку и удалил VM
