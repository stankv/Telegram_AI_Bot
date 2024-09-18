# Асинхронный Telegram-бот с искусственным интеллектом
### Описание
Асинхронный Telegram-бот, реализован на библиотеках [python-telegram-bot](https://docs.python-telegram-bot.org/en/v21.5/)
и [openai](https://pypi.org/project/openai/1.45.1/)

Бот умеет:
* вести диалог
* помогать практиковаться в приглашении на свидания
* генерировать описания профиля для сайтов знакомств
* помогать создавать сообщения при переписке на сайте знакомств

![0](https://github.com/user-attachments/assets/fa1f2b44-8fe9-4c81-b27e-73383910defb)

![0_2](https://github.com/user-attachments/assets/b186f04a-87ba-4f06-b503-d8a8f82fb0c9)

![1](https://github.com/user-attachments/assets/9f8c91d4-ca0d-45b5-9563-b13cf1adaf3c)

![2](https://github.com/user-attachments/assets/6aa5324c-0c34-476d-b70e-9fb17704d8e7)

![3_gpt](https://github.com/user-attachments/assets/dedf8100-a3ca-4cc5-938a-980196ba9a9c)

![4_date](https://github.com/user-attachments/assets/07cd4111-4bba-45f3-8195-ff2664677478)

![5_date_talk](https://github.com/user-attachments/assets/ad38aa21-7058-43b0-91a8-68dfad514b85)

![6_profile](https://github.com/user-attachments/assets/05fab9b6-459f-4e12-900e-5069bb1988ac)

![7_opener](https://github.com/user-attachments/assets/78883ba8-c47b-49b8-afbc-89b7b68f7301)

![8_message](https://github.com/user-attachments/assets/0d1063f2-0cb6-452e-8abd-e866b00c6133)

---
### Файлы и каталоги проекта

* **bot.py** -  содержит всю логику бота, присылает сообщения пользователю, получает сообщения от пользователя и обрабатывает введенные им команды и нажатия кнопок;
* **gpt.py** - содержит служебный класс ChatGPTService, упрощающий работу бота с ChatGPT;
* **util.py** - содержит "служебные" функции для упрощения логики в **bot.py**;
* **settings.py** - файл настроек, содержит API-ключи (токены) для Telegram и ChatGPT;
* **./DB/db_answers.json** - база данных ответов бота, представляет собой словарь в формате _"вопрос пользователя":"ответ бота"_, может быть расширен пользователем.


---
### Инструкция по сборке и запуску проекта
1. Зарегистрировать Telegram-бот:
    * в Telegram в поле поиска ввести **BotFather**, перейти в чат
    * в чате нажать кнопку "Запустить" или ввести команду **/start**
    * ввести команду **/newbot**
    * ввести имя создаваемого бота, например Tinder AI Bot
    * ввести никнейм нового бота, название должно быть уникальным и заканчиваться на **bot**
    * скопировать токен и вставить его в файле **settings.py**
    * перейти в чат созданного бота по ссылке из сообщения я токеном
2. Получить токен для работы с ChatGPT:
    * зарегистрироваться на [chat.openai.com/auth/login](chat.openai.com/auth/login)
    * перейти на сайт: [platform.openai.com](platform.openai.com)
    * на сайте нажимаем Personal, и выбираем **View API keys**
    * затем нажимаем **Create new secret key**
    * полученный токен вставляем в файле **settings.py**
3. Установка, сборка и запуск бота:
    * Скачать и установить интерпретатор Python - https://www.python.org/downloads/

      Далее выполнить следующие команды в консоли:

    * **cd <имя_каталога>** # перейти в каталог где будет проект
    * **git clone https://github.com/stankv/Telegram_AI_Bot.git** # клонировать репозиторий
    * **cd Telegram_AI_Bot** # перейти в каталог проекта
    * **pip install -r requirements.txt** # установить пакеты и зависимости
    * **python bot.py** # запустить телеграм-бот

