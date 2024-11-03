# Домашнее задание к лекции "Контейнеры"

## Слайды из лекции

[Тут](https://nextcloud.buymov.ru/s/sfipBKDKXr9tMgn/download/containers.pdf)

## Задание

Нужно написать "свой докер", т.е. программу для запуска проложения в контейнере. Можно использовать любой язык.

Достаточно реализовать:

- ограничения по CPU и RAM
- mnt ns
- pid ns

Пример:

```bash
./mydocker run --mem 100M --cpu 1.0 --root rootfs.tar /bin/bash
```

В данном случае должен запуститься bash, который будет иметь указанные ограничения по памяти и CPU, у него должен быть PID = 1 и файловая система из rootfs.tar (chroot)

Подсказка, как можно получить rootfs из любого образа:

```bash
[root@localhost ~]# docker images | grep 57f00a4dcc60
docker.io/library/almalinux                   latest      57f00a4dcc60  3 weeks ago    213 MB
[root@localhost ~]# docker export $(docker create 57f00a4dcc60) --output="rootfs.tar"
```

## Результаты

- выложить на github, расшарить с `byumov@gmail.com`
- сообщить о готовности: [https://vk.com/byumov](https://vk.com/byumov)

## Дедлайн

8 ноября 2024
