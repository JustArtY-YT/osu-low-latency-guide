Данный гайд является обновлённым гайдом от [Vudek'a](https://osu.ppy.sh/u/Vudek)
# 0 этап: Подготовка
## Рассматривается вариант установка отдельный диск (SSD)

(Напишите подготовку сами, мне впадлу, да и винды давно нет)

После загрузки на флешку у вас будет один из вариантов экрана:

![boot_bios.png](../photos/boot_bios.png)
![boot_uefi.png](../photos/boot_uefi.png)

Выбирайте первый пункт
# 1 этап: Установка
## 1.1 Подготовка
После загрузки у вас должно быть следующим образом:
![Arch_start.png](../photos/arch_start.png)
Сначала проверим интернет соединение командой `ping`
![ping.png](../photos/ping.png)
Если запросы идут, значит интернет есть.

Чтоб закончить нажмите Ctrl+C

Если вы используйте Wi-Fi, то надо воспользоваться утилитой `iwd`

К сожалению, я не могу продемонстрировать это в данном руководстве, но если вы сможете помочь мне, пожалуйста, сделайте PR

В противном случае, подключите телефон через провод к вашему компьютеру и раздайте интернет через него
## 1.2 Установка
После того, как мы убедились в подключении к сети, запускаем `archinstall`

![archinstall.png](../photos/archinstall.png)

После загрузки у вас будет такое меню:

![menu.png](../photos/menu.png)
# 1.2.1 Зеркала
Пропускаем первые два пункта, начинаем с `Mirrors`

Управление производится стрелками и Enter

После открытия меню `Mirrors` будет следующее:

![mirror_region.png](../photos/mirror_region.png)

Выбираем `Mirror region`

В меню выбирайте свою страну. Чтоб легче найти свою страну, нажмите `/` и пишите свою страну на английском, потом нажимаете `Enter`

![regions.png](../photos/regions.png)

Должно быть так (В моём случае `Russia`):

![mirror_result.png](../photos/mirror_result.png)
## 1.2.2 Разметка дисков
Затем `Disk configuration`:

![partitioning.png](../photos/partitioning.png)
Выбираем `Partitioning`

![best-effort.png](../photos/best-effort.png)

Выбираем `Use a best-effort default partiotion layout`

![sel_disk.png](../photos/sel_disk.png)

Так как я на виртуалке, тут один диск, а вы должны выбрать свой нужный

Выбираем файловую систему:

![btrfs.png](../photos/btrfs.png)

Выбираем `btrfs` как более быструю файловую систему

![subvolumes.png](../photos/subvolumes.png)

Выбираем `No`

![compression.png](../photos/compression.png)

Выбираем `Use compression`

Должно быть вот так:

![disk_result.png](../photos/disk_result.png)
## 1.2.3 Шифрование диска
Пропускаем пункт `Disk encryption`, но можете сделать.
## 1.2.4 Файл подкачки
Убедимся, что `swap` включён:
![swap.png](../photos/swap.png)
## 1.2.5 Загрузчик
`Bootloader` выбираем Grub
![bootloader.png](../photos/bootloader.png)
## 1.2.6 Унифицированные образы ядра
Оставляем `Unified kernel images` по дефолту (Disabled)
![UKI.png](../photos/UKI.png)
## 1.2.7 Хостнейм
Можете оставить по дефолту, либо написать свой. В терминале будет вот так: `username@hostname $`
![hostname.png](../photos/hostname.png)
## 1.2.8 Пароль рута
![](../photos/Pasted%20image%2020250304224042.png)
# 2. Загрузка в установленную ОС
