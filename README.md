Цель лабораторной работы
Научиться тестировать проекты с помощью юнит-тестов.
Предусловия:
Созданный примитивный файловый менеджер.
Программа должна работать в определенной папке (рабочей папки
менеджера) и позволять пользователю выполнять следующие простые
действия в пределах рабочей папки:
1. Создание папки (с указанием имени);
2. Удаление папки по имени;
3. Перемещение между папками (в пределах рабочей папки) - заход в
папку по имени, выход на уровень вверх;
4. Создание пустых файлов с указанием имени;
5. Запись текста в файл;
6. Просмотр содержимого текстового файла;
7. Удаление файлов по имени;
8. Копирование файлов из одной папки в другую;
9. Перемещение файлов;
10. Переименование файлов.
Задание:
Необходимо написать тесты, которые проверяют работу файлового
менеджера.
Покрытия тестами составляет от 80%
Указания к выполнению
1. Библиотека для тестирования Pytest
2. Использовать технику позитивного и негативного тестирования

3. Использовать технику граничных условий и классов эквивалентности
4. Разработка должна вестись с использованием СКВ Git. Код должен
публиковаться в репозитории на GitHub.
5. Файл README.md должен содержать описание созданных тестов и
скриншот с отчетом о запуски и прохождением тестов.

Структура проекта:

![image](https://user-images.githubusercontent.com/92279258/147479282-48f83520-9aa1-4cce-89b1-657a31d0d5da.png)

Как видим, в отдельную директорию tests был добавлен файл с тестами, который называется test_functions

![image](https://user-images.githubusercontent.com/92279258/147479507-6cd4349f-3efe-4caf-974b-9323f206735d.png)

Также ниже находится файл manager.py, который содержит сам файловый менеджер 

PyCharm позволяет нам подгрузить библиотеку Pytest в конфигурацию проекта, нужно только назначить рабочую папку tests

![image](https://user-images.githubusercontent.com/92279258/147479742-c643c435-cd6b-4cff-992c-6ac7b8b56579.png)

.pytast_cashe - созданная библиотекой директория с лог файлами.

Алгоритм тестировки будет проводиться с использованием фикстур. Пример:

![image](https://user-images.githubusercontent.com/92279258/147480222-016c08b5-3a19-4620-994c-cc91abe6e639.png)

Сам тест: 

![image](https://user-images.githubusercontent.com/92279258/147480344-18c5ec30-d092-4607-aef5-6d6f62d97abd.png)

Логика проверки проста - выполнение того или иного действия фиксируется в самой программе на True или False, а тест сверяет значение с ожидаемым.

Также в директории .pytast_cashe имеется файл, который содержит следующую информацию: 

![image](https://user-images.githubusercontent.com/92279258/147480615-47e4f069-b075-4499-879b-a8dd1142fc94.png)

Это сильно облегчает проверку, так как в одном месте уже прописаны все тесты

Файл самого менеджера: 

![image](https://user-images.githubusercontent.com/92279258/147481052-61e05d31-647e-457a-9d56-8255afe48d7f.png)

Итоговые результаты тестирования: 

![image](https://user-images.githubusercontent.com/92279258/147480820-3f63df57-86d1-41b1-a6b7-7ed22bdcad70.png)

![image](https://user-images.githubusercontent.com/92279258/147480961-2b0afb29-d6d7-4c81-b5ce-7d7e50359b96.png)


