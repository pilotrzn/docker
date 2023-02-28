### список всех контейнеров

```bash 
$ docker ps -a
```
### Список запущенных контейнеров

```bash
$ docker ps
```

### Список локальных образов

```bash
$ docker images
```

### Скачивание образа. Образ будет только скачан на компьютер

```bash
docker pull hello-world
```

### Создание контейнера из образа. Здесь указан образ hello-world - официальный образ докера

```bash
docker run hello-world
$ docker ps -a
CONTAINER ID   IMAGE         COMMAND    CREATED         STATUS                     PORTS     NAMES
a11bd415ff07   hello-world   "/hello"   2 minutes ago   Exited (0) 2 minutes ago             vibrant_jang
```

### Удаление контейнера. При удалении указывается container id

```bash
$ docker rm a11bd415ff07
```

### Подключение к интерактивному терминалу контейнера

```bash
$ docker run -it busybox
```

### Контейнер с именем

```bash
$ docker run -d --name name_of_container image_name
```

### Удаление всех остановленных контейнеров

```bash
$ docker container prune
```

### Получить информацию про контейнер

```bash
$ docker container inspect {container_id}
```

### Узнать ip адрес контейнера

```bash
~$ docker exec -it {container_id} bash
:/# hostname -i
```

Дополнительно можно сделать grep для вывода, если нужно получить определенную строку


### Остановка контейнера

```bash
$ docker stop {container_id}
```