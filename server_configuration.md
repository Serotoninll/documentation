# Конфигурация сервера

## Операционные системы

- **Windows Server 2019**: Основная операционная система для корпоративной сети.
- **Ubuntu Server 20.04**: Используется для разработки и тестирования.

## Шаги по установке Ubuntu Server

1. Скачайте образ Ubuntu Server с [официального сайта](https://ubuntu.com/download/server).
2. Запишите образ на USB-накопитель.
3. Загрузитесь с USB-накопителя и следуйте инструкциям на экране для установки.

## Настройка SSH

1. Установите OpenSSH Server:
   
bash
   sudo apt update
   sudo apt install openssh-server -y
  
2. Проверьте статус службы SSH:
   
bash
   sudo systemctl status ssh
  

## Настройка брандмауэра

1. Установите UFW:
   
bash
   sudo apt install ufw -y
  
2. Разрешите соединения по SSH:
   
bash
   sudo ufw allow OpenSSH
  
3. Включите UFW:
   
bash
   sudo ufw enable
