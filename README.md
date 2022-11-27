# Inception
### Цели данного проекта:
- Расширение знаний в области системного администрирования с помощью Docker
- Виртуализация нескольких образов Docker на виртуальной машине
### Subject
[subject](https://github.com/luta-wolf/inception/tree/main/pdf/inc_subject.pdf)
### Теоретический материал
- [Docker и Docker-Compose Tutorial](https://ivan-shamaev.ru/docker-compose-tutorial-container-image-install/)
- [Руководство по Docker Compose для начинающих](https://habr.com/ru/company/ruvds/blog/450312/)
- [Nginx, Php-Fpm и что это вообще?](https://perfect-inc.com/journal/nginx-php-fpm-i-chto-eto-voobshche/)
- [MariaDB](https://ru.wikipedia.org/wiki/MariaDB)
- [Установка WordPress с помощью Docker Compose](https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-with-docker-compose-ru)
### Определения
- `Docker` – это технология, которая решает проблемы развертывания и масштабирования путем отделения приложений от зависимостей инфраструктуры. Она решает эти проблемы благодаря применению контейнеров, позволяющих упаковать приложение со всеми его зависимостями, включая структуру каталогов, метаданные, пространство процессов, номера сетевых портов и т. д. Приложение, упакованное в контейнер, запускается одинаково на любых машинах и в любых окружениях.
- `Dockerfile` — это текстовый файл конфигурации, написанный с использованием специального синтаксиса. В нем описываются пошаговые инструкции по всем командам, которые необходимо выполнить для сборки образа Docker.
- `Docker-compose` — это система сборки, запуска и управления множеством контейнеров. Docker-compose не входит в единый пакет поставки Docker и устанавливается отдельно. Для сборки кластера контейнеров используется docker-compose.yml.
- `Docker-compose.yml` — конфигурационный файл в YAML-формате, описывающий логику запуска и взаимодействия контейнеров между собой и внешним миром. В сущности инструкции заложенные в docker-compose.yml по логике работы идентичны ключам команды docker run.
- `Docker vs virtual machine` - основное различие между контейнерами и виртуальными машинами заключается в том, что контейнеры охватывают только уровень приложения и полагаются на базовое ядро ​​операционной системы, в случае виртуальной машины создается новый экземпляр операционной системы.

### Гайды
- [Гайд](https://github.com/codesshaman/inception)  от jleslee
- [Гайд](https://github.com/rbiodies/Inception/blob/main/README.md) от rbiodies


### Работа с вирутальной машиной из `VC Code`
1. Установи плагин Remote - SSH
2. Окрой командную сроку (нажать `⇧``⌘``P` или Shift + Command + P на школьных маках)
3. Введи / выбери `Remote-SSH: Add New SSH Host`
4. Пишем соединение по ssh `ssh root@localhost -p 42`
5. Выбираем `/Users/einterdi/.ssh/config`  и жмакаем на кнопку `Подключиться`
6. В нижнем левом углу VS Code нажимаем на зеленый значек соединения
7. В открывшейся командной строки выбирай  `Connect to Host`, выбери `localhost`, введи пароль (от root пользователя виртуалки) и работай

### Команды
- `docker --help` - показать все доступные команды
- `docker info` - информация по докерам
- `docker ps` - вывести список докеров
- `docker images` - вывести образы и их размеры
- `docker stop <имя_контейнера>` - останавливает выбранный контейнер
- `docker start <имя_контейнера>` - запускает выбранный контейнер
- `docker restart <имя_контейнера>` - перезапускает выбранный контейнер
- `docker exec -it mariadb mysql -u root` - позволяет зайти в бд MariaDB
  - `show databases;` - просмотр бд

### Checklist
[checklist](https://github.com/luta-wolf/inception/tree/main/pdf/inc_check.pdf)
