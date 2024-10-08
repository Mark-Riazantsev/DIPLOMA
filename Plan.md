# Тест-план по тестированию мобильного приложения Хоспис

## Описание ПО:

Приложение предоставляет возможности для работы с новостями хосписа и включает:

- информацию о новостях и инструменты для их обработки;
- тематические цитаты;
- сведения об самом приложении.

## Границы приложения и реализованный функционал:

1. Страница авторизации, на которой есть:

- Поле для ввода "Логин"
- Поле для ввода "Пароль"
- Кнопка "Войти"

2. Главный экран

- Верхнее меню с кнопками

* Бергерменю разделами "Главная", "Новости", "О приложении"
* Вкладка "Love is all" с тематическими цитатами
* Кнопка выхода (Log out)

- Основной экран

* Раздел "Новости", с разворотом и переходом на ALL NEWS

## Задачи тестирования

Проверить работу авторизации, отображение новостей и цитат. Составить рекомендации по повышению качества разработки программного обеспечения.

## Типы тестирования

Планируется провести следующие типы тестирования:

### По степени автоматизации

Ручное
Автоматизированное (smoke UI, регресс UI)

### Функциональное тестирование

Загрузка приложения

Авторизация

Выход из приложения

Меню приложения

Блок "Главная"

Блок "Новости" (Чтение новости, Фильтрация новостей по дате создания и по категории, Сортировка новостей, Переход в "Панель управления")

Блок "Панель управления"(Создание новости, Редактирование новости, Изменение статуса (активна/не активна), Удаление новости, Фильтрация новостей по дате создания и по категории, Сортировка новостей)

Блок "О приложении"

Блок цитат о хосписе

### Проверки специфичные для мобильного приложения области

Проверки при разных состояниях сети Интернет

Работа с функциями телефона (ориентация, жесты)

### Тестирование совместимости (высокий уровень приоритености)

Установка и работа основных функций на устройствах с разными версиями Android, различными разрешениями экрана

### UI/UX - тестирование (низкий уровень приоритетности)

Соответствие макету
Оценка удобства пользования

### Тестирование безопасности (средний уровень приоритетности)

SQL-инъекции
XSS-инъекции

### Тестирование локализации

Все должно быть на русском языке

## Документация

- План тестирования
- Чек-лист
- Тест-кейсы

## **Окружение для тестирования на мобильном устройстве**

Устройство (эмулятор): Google Pixel
Модель: 7
Версия Android: 10
Разрешение: 1080 x 2400 px
Память: 5,6 GB
RAM: 2 GB

## **Окружение для тестирования на ПК**

Процессор: Intel(R) Core(TM) i5-4200M CPU @ 2.50GHz 2.50 GHz
Оперативная память: 16.0 ГБ (доступно: 15.9 ГБ)
Тип системы: Windows 10 Домашняя, 64-разрядная операционная система, процессор x64

## **Тестовая документация**

- План тестирования по проверке и автоматизации приложения
- Чек-лист
- Тест-кейсы
- Баг-репорты
- Отчет о тестировании
- Результат сравнения времени проверки приложения по чек-листу руками и ui-тестами

## **Техники тест дизайна с обоснованиями**

1. Техники классов эквивалентности и граничных значений для проверки валидации полей: логин, категория новостей, заголовки, описания, пароль.
2. Техника состояний и переходов (для функции модераций, создания, редактирования и удаления в новостном блоке)

## Перечень используемых инструментов

1. Git-hub - для хранения кода и автотестов.

- Android Studio - создание эмуляторов, установка проекта, ручные проверки, написание кода тестов;
- Фреймворк для тестирования Espresso - для записи, редактирования и запуска тестов;
- Allure - создание и отправка отчётов;
- Java - широко используемый язык написания автотестов.

### Перечень возможных рисков

- **Высокие начальные затраты времени и ресурсов** - Разработка и настройка автоматических тестов может потребовать значительных временных и ресурсных затрат на начальном этапе, что может быть не выгодно для небольшого проекта.
- **Изменения в приложении** - Частые изменения в приложении могут привести к необходимости регулярной актуализации тест-кейсов и автотестов, что может увеличивать затраты времени и усилий на поддержку тестов. Также в возможно изменение названия полей, изменение текста предупреждений об ошибке и т.д.
- **Поддержка и обновление тестов** - Автотесты требуют регулярной актуализации и поддержки по мере развития приложения. Иначе тесты могут стать устаревшими, неактуальными и выдавать некорректный результат.
- ***

### Интервальная оценка с учетом рисков

- Написание тест-плана: 11-12 часов
- Написание чек-листа: 6 часов
- Написание тест-кейсов
  - Без рисков: 22 часа
  - С учетом рисков: 24 часа
- Написание автоматизированных тестов: 35 часов
- Создание отчетности: 12 часов

### Порядок выполнения работ

- Составление плана тестирования

- Составление чек-листа

- Написание тест-кейсов
- Ручное тестирование

- Написание автотестов

- Проведение автотестирования

- Формирование отчета о тестировании

### Сортировка тест-кейсов по степени автоматизации

_Автоматизация_

Обязательно нужно включить авторизацию, базовые функции по работе с новостями(например обязательно добавление новости) и.т.д. Также другие страницы приложения(о приложении, цитаты).

- Валидация поля "Логин" - 1
- Валидация поля "Пароль" - 2
- Авторизация зарегистрированного пользователя и выход из профиля - 5
- Авторизация незарегистрированного пользователя - 3
- Авторизация пользователя с неверным паролем - 4
- Авторизация пользователя с пустыми полями - 6
- Переход по разделам Action menu - 12
- Переход на страницу "Все новости" из раздела "Главная" - 13
- Чтение новости в разделе "Главная" - 26
- Добавление новости с заполненными полями - 29
- Добавление новости с незаполненными полями - 30
- Удаление новости - 40
- Заполнение поля Описание в форме добавления новости - 36
- Сохранение формы "Редактирование новости" после внесенных изменений - 37
- Сортировка списка новостей - 41
- Фильтрация новостей по категории - 42
- Фильтрация новостей по дате публикации - 43
- Чтение новости - 44
- Переход по ссылкам в разделе "О приложении" - 45

_Ручное тестирование_

Остальные тест-кейсы (7-11, 14-25, 27,28, 31-35, 38, 39, 46, 47)

### Критерии начала тестирования

Приложение загружается, устанавливается на телефон или эмулятор, запускается, и можно выполнить авторизацию с помощью логина и пароля.

### Критерии окончания тестирования

Нет критических багов
