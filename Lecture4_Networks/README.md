# ДЗ

## Админское [2 балла]
1. На двух ВМ создать виртуальное устройство `dummy0` и настроить на нём /32 адрес из приватного диапазона.
   - Статически (файлом конфигурации в `systemd-networkd`/`NetworkManager`) [1 балл]
   - Динамически (командами `ip ...`) [0.5 балла]
2. Настроить маршрутизацию между /32
   - bird + BGP [1 балл]
   - Статические маршруты (`ip r a ...`) [0.5 балла]
3. Обменяться данными между /32 адресами этих ВМ

## Программистское [3 балла]
Написать программу для DNS резолва (A/AAAA записи) через произвольный DNS сервер.
Сетевое взаимодействие организовать через RAW сокет (`SOCK_RAW`). Сформировать UDP пакет, отправить и получить и вывести ответ. [3 балла]

## Проверка
### для проверки
- выложить результат на  github, расшарить с trfmov@gmail.com
- сообщить о готовности https://vk.com/trfmov

### ожидаемые результаты
- конфиги/команды настройки
- исходники
- вывод команд

### сроки
Последний день приёма работ **18 октября 2024**.