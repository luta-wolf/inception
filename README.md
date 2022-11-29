# Inception
### Цели данного проекта:
- Расширение знаний в области системного администрирования с помощью Docker
- Виртуализация нескольких образов Docker на виртуальной машине
## Subject
[subject](https://github.com/luta-wolf/inception/tree/main/pdf/inc_subject.pdf)

<img width="684" alt="image" src="https://user-images.githubusercontent.com/58044383/204354456-d5980b8f-4001-44c4-a6dd-1594a28178c0.png">

## Теоретический материал
- [Docker официальная документация](https://docs.docker.com/)
- [Docker и Docker-Compose Tutorial](https://ivan-shamaev.ru/docker-compose-tutorial-container-image-install/)
- [Образы и контейнеры Docker в картинках](https://habr.com/ru/post/272145/)
- [Docker самый простой и понятный туториал](https://badtry.net/docker-tutorial-dlia-novichkov-rassmatrivaiem-docker-tak-iesli-by-on-byl-ighrovoi-pristavkoi/)
- [Руководство по Docker Compose для начинающих](https://habr.com/ru/company/ruvds/blog/450312/)
- [Nginx, Php-Fpm и что это вообще?](https://perfect-inc.com/journal/nginx-php-fpm-i-chto-eto-voobshche/)
- [MariaDB](https://ru.wikipedia.org/wiki/MariaDB)
- [Установка WordPress с помощью Docker Compose](https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-with-docker-compose-ru)
## Определения
- `Docker` – это технология, которая решает проблемы развертывания и масштабирования путем отделения приложений от зависимостей инфраструктуры. Она решает эти проблемы благодаря применению контейнеров, позволяющих упаковать приложение со всеми его зависимостями, включая структуру каталогов, метаданные, пространство процессов, номера сетевых портов и т. д. Приложение, упакованное в контейнер, запускается одинаково на любых машинах и в любых окружениях.
- `Docker-compose` — это система сборки, запуска и управления множеством контейнеров. Docker-compose не входит в единый пакет поставки Docker и устанавливается отдельно. Для сборки кластера контейнеров используется docker-compose.yml.
- `Docker-compose.yml` — конфигурационный файл в YAML-формате, описывающий логику запуска и взаимодействия контейнеров между собой и внешним миром. В сущности инструкции заложенные в docker-compose.yml по логике работы идентичны ключам команды docker run.
- `Docker vs virtual machine` - основное различие между контейнерами и виртуальными машинами заключается в том, что контейнеры охватывают только уровень приложения и полагаются на базовое ядро операционной системы, в случае виртуальной машины создается новый экземпляр операционной системы.
- `Dockerfile` — это текстовый файл конфигурации, написанный с использованием специального синтаксиса. В нем описываются пошаговые инструкции по всем командам, которые необходимо выполнить для сборки образа Docker. Файл создаётся по принципу «одна строка — одна команда».
- `Daemon` - фоновая служба на хосте, которая отвечает за создание, запуск и уничтожение контейнеров.
- `Image` - неизменяемый файл (образ), из которого можно неограниченное количество раз развернуть контейнер.
- `Client` - утилита командной строки в Docker для управления демоном. Любое взаимодействие с контейнером проходит через Daemon.
- `Container` - запущенное приложение, которое развернули из образа.
- `Registry` - служба в Docker, выполняющая функции репозитория (хранилища). Позволяет следить за версиями образов, создавать приватные репозитории.
- `Docker Desktop` - приложение, позволяющее локально собирать, выполнять и тестировать контейнеры. Работает на Windows и macOS.
- `Docker volumes` - тома для постоянного хранения информации. По умолчанию в Docker папки хранилищ создаются на хост-машине, но предусмотрена и возможность подключения удаленных хранилищ. Использование томов позволяет лучшим образом настроить хранение данных.
## Гайды
- [Гайд](https://github.com/codesshaman/inception)  от jleslee
- [Гайд](https://github.com/rbiodies/Inception/blob/main/README.md) от rbiodies
- [Видеогайд](https://www.youtube.com/watch?v=Veuv7MjaIKQ&t=3119s&ab_channel=Edu_events_mow) от meunostu
## Работа с вирутальной машиной из `VC Code`
1. Установи плагин Remote - SSH
2. Окрой командную сроку (нажать `⇧``⌘``P` или Shift + Command + P на школьных маках)
3. Введи / выбери `Remote-SSH: Add New SSH Host`
4. Пишем соединение по ssh `ssh root@localhost -p 42`
5. Выбираем `/Users/einterdi/.ssh/config`  и жмакаем на кнопку `Подключиться`
6. В нижнем левом углу VS Code нажимаем на зеленый значек соединения
7. В открывшейся командной строки выбирай  `Connect to Host`, выбери `localhost`, введи пароль (от root пользователя виртуалки) и работай
## Команды
Команды `docker` работают из любой директории
- `docker --help` - показать все доступные команды
- `docker info` - информация по докерам
- `docker ps` - вывести список докеров
- `docker images` - вывести образы и их размеры
- `docker network ls` - вывести все сетевые соединения
- `docker volume ls` - вывести все volume
- `docker exec -it <имя_или_id_контейнера> /bin/sh` - зайти в контейнер (ядро  alpine)
- `docker exec -it <имя_или_id_контейнера> /bash` - зайти в контейнер (ядро debian buster)
- `docker stop <имя_или_id_контейнера>` - останавливает выбранный контейнер
- `docker start <имя_или_id_контейнера>` - запускает выбранный контейнер
- `docker restart <имя_или_id_контейнера>` - перезапускает выбранный контейнер
- `docker exec -it mariadb mysql` - позволяет зайти в бд MariaDB под пользователем
- `docker exec -it mariadb mysql -u root` - позволяет зайти в бд MariaDB под root
  - `show databases;` - просмотр бд

Команды `docker-compose` работают из директории, где находится файл docker-compose.yml
- `docker-compose --help` - показать все доступные команды
- `docker-compose ps` - вывести список докеров
- `docker-compose up -d` - запускает контейнеры по образам
- `docker-compose stop` - остановить контейнеры
- `docker-compose down` - остановить и удалить контейнеры, сети, образы и тома
- `docker-compose --build` - создает образы из Dockerfile
- `docker-compose images` вывести образы и их размеры
- `docker-compose kill <имя_или_id_контейнера>` - останавливает выбранный контейнер

## Бонусы
- Настройте кеш Redis для своего веб-сайта WordPress, чтобы правильно управлять кешем (1).
- Настройте контейнер FTP-сервер, указывающий на том вашего сайта WordPress (2).
- Настроить Adminer (3).
- Создайте простой статический веб-сайт на выбранном вами языке, кроме PHP (да, PHP исключен!). Например, сайт-витрина или сайт для представления вашего резюме (4).
- Настройте сервис по вашему выбору, который вы считаете полезным. Во время защиты вам придется обосновать свой выбор (5).

1. Redis

Устанавливаем его из плагинов wordpress
<img width="1258" alt="image" src="https://user-images.githubusercontent.com/58044383/204343498-47142427-a0d6-4272-b53f-be8be1da8099.png">
2. Vsftpd

Из виртуальной машины запускаем приложение `FileZilla`
```
Host: 127.0.0.1
Username: ftpuser
Password: ftppass
Port: 21
```
<img width="1198" alt="image" src="https://user-images.githubusercontent.com/58044383/204333409-0f995571-6187-4bf9-8c07-afa0957b05d3.png">
3. Adminer

- `http://localhost:8080` - запуск adminer
<img width="638" alt="image" src="https://user-images.githubusercontent.com/58044383/204332432-3241aa4a-904d-4e64-a3a5-839ca041a018.png">
4. Website

- `http://localhost/`
<img width="1140" alt="image" src="https://user-images.githubusercontent.com/58044383/204483777-cc799c62-bb8c-4134-a852-9a7516b51f0e.png">

5. Portainer

Запускаем контейнер portainer отдельно от остальных:
```
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:2.11.1
```
`https://localhost:9443`
```
Login: admin
Password: einterdi
```
<img width="1025" alt="image" src="https://user-images.githubusercontent.com/58044383/204336274-3e9a3910-0114-4cdb-98e9-37d7d4c75f93.png">

## Защита
[checklist](https://github.com/luta-wolf/inception/tree/main/pdf/inc_check.pdf)

- [Видео защиты проекта](https://www.youtube.com/watch?v=nFr3yqEt1W0&ab_channel=%D0%90%D0%BB%D0%B5%D0%BA%D1%81%D0%B0%D0%BD%D0%B4%D1%80%D0%94%D0%B8%D0%B4%D0%B5%D0%BD%D0%BA%D0%BE) от sjacki
## Полезные материалы
- [Docker Hub](https://hub.docker.com/) - популярный публичный репозиторий, куда вы можете загружать свои образы (images) для совместной работы с командой, заказчиками или другими пользователями.
