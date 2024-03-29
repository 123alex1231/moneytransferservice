# [Курсовой проект "Сервис перевода денег"](https://github.com/netology-code/jd-homeworks/blob/master/diploma/moneytransferservice.md)

## Описание проекта

REST-сервис предоставляет интерфейс для перевода денег с одной карты на другую по [заранее описанной спецификации](MoneyTransferServiceSpecification.yaml).
Заранее подготовленное веб-приложение (FRONT) подключается к разработанному сервису без доработок и использует его функционал для перевода денег.

Изначально front доступен на порту 3000, back - на порту 5500.

## Описание реализации

- Приложение разработано с использованием Spring Boot;
- Использован сборщик пакетов MAVEN;
- Для запуска используется docker, docker-compose;
- Код размещен на github;
- Код покрыт unit тестами с использованием mockito;
- Добавлены интеграционные тесты с использованием testcontainers.

## ВАЖНО!!!

[Интеграционный тест](src/test/java/ru/netology/TransferMoneyApplicationTests.java) 
изначально закомментирован, поскольку с ним не получится собрать docker-контейнер.
После сборки docker-контейнера требуется раскомментировать и запустить данный тест.

## Запуск приложения (с docker и без него)

1. Скачать [FRONT](https://github.com/frepingod/netology-transfer-money-front) и выполнить инструкции из него
2. Скачать данный сервис, выполнить maven -> package

#### Для запуска без docker
3. Запустить main метод в классе TransferMoneyApplication.java

#### Для запуска через docker
4. Запустить docker-compose.yml

## Изначальные тестовые данные карт

- **номер карты: 1111111111111111, годен до: 08/26, cvv: 123, сумма: 1000**
- **номер карты: 2222222222222222, годен до: 08/27, cvv: 124, сумма: 1000**
- **номер карты: 3333333333333333, годен до: 08/28, cvv: 125, сумма: 1000**