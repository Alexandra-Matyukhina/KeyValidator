# Отчёт о тестировании <KeyValidator>

## Краткое описание

<2021.05.08 at 9:00 AM> - <2021.05.08. at 10:15 AM> было проведено тестирование методом Black Box, а именно ввод эквивалентных значений в поле для прохождения валидации приложения <KeyValidator>. Так же было произведено тестирование установки и запуска OpenJDK11 для Windows 10 методом Ad-hoc.

На тестирование затрачено: <1 час 15 минут>

В результате тестирования выявлены следующие дефекты:
* [Ключ из валидного списка не проходит валидацию](https://github.com/Alexandra-Matyukhina/KeyValidator/issues/1#issue-880740985)
* [Ключ из невалидного списка проходит валидацию](https://github.com/Alexandra-Matyukhina/KeyValidator/issues/2#issue-880747300)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты*:
* Инструкция по установке OpenJDK 11
* Руководство использования KeyValidator



В качестве тестовых данных использовались данные из [руководства использования KeyValidator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md):

* Валидные ключи:
8f05e6a7-70e9-33d7-bfe7-b19eae0d8998 - result is ok
80b427f8-92cd-3aae-ba04-3927fbe17c6 - result is ok
b295bc63-9f03-3b4b-af80-969b39f8c262 - result is ok
387eedc6-12e9-3b32-9881-63b6b5e85317 - result is ok
c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180 - result is ok

* Невалидные ключи:
18252235-78e0-44a5-8720-556f0c7da17a - result is fail
e66075b6-ddad-445e-baf6-161b3289522b - result is fail
b6d53250-f07e-4352-a293-6102ddf7f1ca - result is fail
c2bc778a-1cb9-46c6-b435-0489649d2a42 - result is fail
2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1 - result is fail

Тестирование производилось в следующем окружении:
* Устройство: Microsoft Surface Laptop 3
* Windows 10
* AdoptOpenJDK JDK with Hotspot 11.0.10+9 (x64)
* IntelliJ IDEA 2021.1.1 (Community Edition), Runtime version: 11.0.10+9-b1341.41 amd64)