### University: ITMO University
### Faculty: FTMI
### Course: Cloud platforms as the basis of technology entrepreneurship
### Year: 2024/2025
### Group: U4225
### Author: Gribkov Savelii Evgenievich
### Lab: Lab1
### Date of create: 04.11.2024
### Date of finished: tbc

# Лабораторная работа 1 - Обзор Google Cloud и исследование ключевых сервисов

## Цель работы: 
Ознакомиться с основными возможностями и преимуществами облачной платформы Google Cloud.
## Ход работы:
1) Получен доступ к Google Cloud
2) Создал service account с ролью Storage Admin
![image](https://github.com/user-attachments/assets/b918c219-be05-4602-86f2-c9a213278d43)

3) Создал минимальный compute engine с Machine type e2-micro в режиме spot.
![image](https://github.com/user-attachments/assets/2e88915f-ab4e-4115-b908-5517919891ee)
![image](https://github.com/user-attachments/assets/73fd0639-1418-4bb4-a789-7edb5d6ff78f)
![image](https://github.com/user-attachments/assets/d96dbd4a-6101-4f52-a242-5ff081ecd062)
![image](https://github.com/user-attachments/assets/cbaba5ca-94e0-4ee2-9e96-842d1749b527)

5) С помощью утилиты gsutils нашел бакет lab1-bucket-itmo и скопировал 3 файла в локальную папку на VM. Отобразил, что эти файлы хранятся на VM
![image](https://github.com/user-attachments/assets/a769506c-4c49-4276-994e-e9bd226e0ce4)

6) Поменял права доступа для service account с Storage Admin на Compute Viewer, попробовал повторить пункт с копированием данных
7) 
![image](https://github.com/user-attachments/assets/03e5ab23-203a-4ff7-a225-b0fd1231b9cb)
![image](https://github.com/user-attachments/assets/3feca786-9757-4546-ad9e-d853ee75c721)
## Итог: Скопировать файлы не удалось
### Вывод:
Роль Storage Admin предоставляет полный контроль над бакетами, папками и объектами. Compute Viewer дает доступ только для чтения и для получения и просмотра информации обо всех ресурсах Compute Engine, включая экземпляры, диски и брандмауэры. Роль Compute Viewer позволяет получать и просматривать информацию о дисках, образах и снимках, но не позволяет читать хранящиеся на них данные, в чем я убедился на шаге 6

7) Произвел очистку и удалил VM
