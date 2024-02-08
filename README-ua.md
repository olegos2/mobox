![logo](docs/img/logo.png "logo")

<a href="https://github.com/olegos2/mobox/tree/main">English</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ru.md">Русский</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
Українська
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pt_BR.md">Português Brasileiro</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pl.md">Polski</a>

##

`Mobox` - це проєкт, розроблений з метою запуску windows x86 додатків у [Termux](https://github.com/termux/termux-app), використовуючи [Box64](https://github.com/ptitSeb/box64) та [Wine](https://www.winehq.org/).

# Встановлення
1. Встановіть
[Termux](https://f-droid.org/repo/com.termux_118.apk),
[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) та
[Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk).

2. Відкрийте termux та вставте команду

```bash
curl -s -o ~/x https://raw.githubusercontent.com/olegos2/mobox/main/install && . ~/x
```

3. Введіть `mobox` у termux.

# Конфігурація 
## Wine
Wine може бути встановлений або видалений у меню `Manage packages`.
Для вибіру контейнера wine, використовуйте опцію 4 у головному меню.
Mesa VirGL, Turnip, Wine Mono та Gecko можуть бути встановлені у Wine Start Menu.
## Налаштування
### Змінні dynarec у Box86 та Box64
Є двоє перемикаючих меню для модифікації змінних dynarec у меню налаштувань mobox.
Подивиться [як використовувати Box64](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md) та [як використовувати Box86](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md), щоб дізнатися більше про змінні dynarec.
### Налаштування системи
Використовуйте меню `System settings` у mobox для локальної модифікації wine, пресета dxvk hud або налаштувань Turnip.
розширення fallback використовується лише коли розширення x11 не може бути виявлено самостійно.
Якщо у вас Snapdragon 8 Gen 1, 8+ Gen 1, 7+ Gen 2, активуйте другу опцію у `select a7xx flickering fix (TU_DEBUG)` у меню `System settings`.
### Root налаштування
Якщо ви маєте Root, то можна використовувати OOM Adjuster, який допомагає зберігати Termux у фоновому режимі.
## Termux-X11 preferences
* `Display resolution mode` exact
* `Display resolution` 1280x720
* `Reseed Screen While Soft Keyboard is open` OFF
* `Fullscreen on device display` ON
* `Force Landscape orientation` ON
* `Hide display cutout` ON
* `Show additional keyboard` OFF
* `Prefer scancodes when possible` ON
## Керування 
Для сенсорного керування потрібен додаток Input Bridge
## Видалення 
Використовуйте меню `Backup and restore` для видалення mobox.
## Налагодження
Для того щоб включити налагодження - оберіть опцію 2 у меню Mobox -> Settings -> Debug settings. Шлях до логів - /sdcard/mobox_log.txt

## Підтримка
### Android
* Рекомендовано `Android 10` або вище.
### Пристрій
* Більшість Android телефонів можуть запустити `mobox` та ігри з DirectX 9, використовуючи Mesa VirGL.
* Рекомендовано пристрії з Snapdragon з Adreno 6xx або Adreno 725-740 для отримання кращої продуктивності і сумісності з Turnip+DXVK.
### Root
* Root не потрібен.

## Знайомі проблеми
* Якщо termux вилітає, коли ви намагаєтеся зайти до меню mobox, видаліть користувацькі скрипти тем:
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* У деяких пристроїв можуть бути проблеми із зависаннями створення префіксу при встановленні PhysX, у такому випадку зміните налаштування у меню `Compatibility settings`
* Для пристроїв з SD845, вимкніть dri3 у меню `Compatibility settings`

## Підтримка mobox
[boosty](https://boosty.to/olegos/donate)

#
Велике спасибі Hugo, JeezDisReez, ptitSeb, MishkaKolos, Xanzo, Jotaros, Maxython, Swed та іншим за їх допомогу.

[MishkaKolos Discord](https://discord.gg/ZAQnZzbCXq)


## Сторонні додатки

[glibc-packages](https://github.com/termux-pacman/glibc-packages)

[Box64](https://github.com/ptitSeb/box64)

[Box86](https://github.com/ptitSeb/box86)

[DXVK](https://github.com/doitsujin/dxvk)

[DXVK-ASYNC](https://github.com/Sporif/dxvk-async)

[DXVK-GPLASYNC](https://gitlab.com/Ph42oN/dxvk-gplasync)

[VKD3D](https://github.com/lutris/vkd3d)

[D8VK](https://github.com/AlpyneDreams/d8vk)

[Termux-app](https://github.com/termux/termux-app)

[Termux-x11](https://github.com/termux/termux-x11)

[Wine](https://wiki.winehq.org/Licensing)

[wine-ge-custom](https://github.com/GloriousEggroll/wine-ge-custom)

[Mesa](https://docs.mesa3d.org/license.html)

[mesa-zink-11.06.22](https://github.com/alexvorxx/mesa-zink-11.06.22)

[Mesa-VirGL](https://github.com/alexvorxx/Mesa-VirGL)

