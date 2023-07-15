# social_network_test_case
Простой RESTful API с использованием FastAPI для приложения социальной сети.
Должна быть какая-то форма аутентификации и регистрации (JWT, Oauth, Oauth 2.0 и т.д.).
Реализована аутентификация и авторизация по JWT
Пользователь имеет возможность зарегистрироваться и войти в систему
Пользователь может создавать, редактировать, удалять и просматривать посты.
А также лайкать и дизлайкать посты

### Документация
Документация доступна по адресу
```
/docs
```

## Запуск
Укажите свои данные в файл .env

#### Установите зависимости
```
pip install -r requirements.txt
```

#### Проведите миграции
```
alembic upgrade head
```
#### Запустите сервер
```
uvicorn src.main:app --reload 
```

### Docker
Для запуска используйте команду
```bash
  make app
```
Или
```bash
  docker-compose -f docker-compose.yml up --build -d
```
Для остановки приложения используете команду:
```
make stop
```
или 
```
docker-compose down
```

## Тесты
Укажите свои данные для подключения к тестовым базам данных в .env
#### Установите зависимости
```
pip install -r requirements.txt
```

#### Запустите тесты командой 
```
pytest
```
