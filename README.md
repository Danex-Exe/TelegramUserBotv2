# Инструкция по установке

### 0. Клонируем репозиторий
    git clone https://github.com/Danex-Exe/TelegramUserBot2.git
###
    git config --global --add safe.directory Путь_до_репозитория

### 1. Устанавливаем необходимые модули
    pip install -r requirements.txt
###
    git clone https://github.com/Danex-Exe/databaze.git
### 2. Первый запуск приложения (Нужен для создания файлов конфигурации)
    python app.py
### 3. Переходим на **[сайт](https://my.telegram.org/auth)** и входим в свой телеграм аккаунт
### 4. Переходим во кладку **[API development tools](https://my.telegram.org/apps)**
### 5. Регистрируем наше приложение
### 6. Открываем файл `./configs/data.json` и записываем в словарь полученные данные бота
    {
        "bot": {
            "current_session": "account",
            "api_id": "00000000",
            "api_hash": "4Df819d0cb8a7Fasd"
        },
        "users": {}
    }
### 7. Запускаем бота
    python app.py
### 8. Указываем свой номер телефона
### 9. Указываем полученный код (Он приходит на ваш Telegram)
### 10. Поздравляю, теперь вы успешно завершили установку и запуск бота!

## Примечание
### 1. Данные хранятся у вас на устройстве и никак сами по себе не могут попасть в чужие руки
### 2. Если вы удалите папку или содержимое папки `./sessions` то у вас пропадет активная сессия вашего телеграм аккаунта. Ее можно восстановить перезапустив программу
### 3. Если файлы из папки `./sessions` попадут в руки другого человека, то он без проблем сможет зайти на ваш телеграм аккаунт. Поэтому советую их никому не передавать
### 4. Для авторизации и использования другого телеграм аккаунта измените название сессии в файле `./congigs/data.json`
    {
        "bot": {
            "current_session": "other_account",
            "api_id": "00000000",
            "api_hash": "4Df819d0cb8a7Fasd"
        },
        "users": {}
    }
