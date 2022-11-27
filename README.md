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
- `docker info` - информация по докерам
- `docker ps` - вывести список докеров
- `docker images` - вывести образы и их размеры
- `docker stop <имя_контейнера>` - останавливает выбранный контейнер
- `docker restart <имя_контейнера>` - перезапускает выбранный контейнер
- `docker exec -it mariadb mysql -u root` - позволяет зайти в бд MariaDB
  - `show databases;` - просмотр бд

### Checklist
[checklist](https://github.com/luta-wolf/inception/tree/main/pdf/inc_check.pdf)
