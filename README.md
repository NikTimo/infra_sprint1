# Финальный проект спринта 11.
## Деплой прижения Kittygram на удаленный сервер
Kittygram - приложение для анкетирования и обмена фотографиями свуоих питомцев.
Можно:
- загружать фотграфии с описанием,
- редактировать фотографии своих питомцев
- просматривать фотошграфии других пользователей
## Стек технолгий:
- backend: Django,
- frontend: React,
- WSGI-server: gunicorn,
- Web-server: NginX.
## Запуск проекта:
Клонировать репозиторий
~~~bash  
git clone https://github.com/NikTimo/infra_sprint1.git
~~~
Создать виртуальное окружени, установить зависимости, выполнить миграции:
~~~bash
cd infra_sprint1
python3.9 -m venv venv
pip install -r requirements.txt
source venv/bin/activate
python backend/manage.py migate
~~~
Запустить frontend и backend
~~~bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
npm i
npm run start
python manage.py runserver
~~~
## Для запуска проекта в постоянную работу предусмотрены конфигурациооные файлы для Gunicorn и NginX в папке infra.
## Автор: NT
