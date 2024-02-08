![logo](docs/img/logo.png "logo")

<a href="https://github.com/olegos2/mobox/tree/main">Angielski</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ru.md">Русский</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ua.md">Українська</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pt_BR.md">Português Brasileiro</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
Polski


##

`Mobox` jest aplikacją zaprojektowaną aby uruchamiać aplikacje x86 w programie [Termux](https://github.com/termux/termux-app) wykorzystując [Box64](https://github.com/ptitSeb/box64) oraz [Wine](https://www.winehq.org/).

# Instalacja
1. Zainstaluj
[Termux](https://f-droid.org/repo/com.termux_118.apk),
[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) oraz
[Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk).

2. Otwórz termux i wklej komendę
```bash
curl -s -o ~/x https://raw.githubusercontent.com/olegos2/mobox/main/install && . ~/x
```

3. Wpisz `mobox` w termux

# Konfiguracja
## Wine
Wine może być zainstalowane lub odinstalowane w menu `Manage packages`.
Aby wybrać kontener wine, użyj opcji 4 w menu głównym.
Mesa VirGL, Turnip, Wine Mono i Gecko mogą zostać zainstalowane z Menu Start (Wine).
# Ustawienia
### Zmienne dynarec Box86 i Box64
Są dwa dedykowane menu aby zmienić ustawienia dynarec w konfiguracji mobox.
Aby dowiedzieć się więcej, zobacz [Box64 usage](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md) oraz [Box86 usage](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md)
### Ustawienia systemowe
Aby zmienić język wine, konfigurację DXVK HUD lub Turnip użyj sekcji `System settings` w mobox.
Rozdzielczość fallback powinna być ustawiona jeżeli oryginalna x11 nie jest w stanie wykryć się automatycznie.
Jeżeli posiadasz Snapdragon 8 Gen 1, 8+ Gen 1, 7+ Gen 2 odblokuj opcję `select a7xx flickering fix (TU_DEBUG)` w sekcji `System settings`.
### Ustawienia root
Jeżeli posiadasz roota, możesz użyć OOM Adjuster aby zapobiec ubijaniu procesów przez wysokie zużycie pamięci.
## Ustawienia Termux-X11
* `Display resolution mode` exact
* `Display resolution` 1280x720
* `Reseed Screen While Soft Keyboard is open` OFF
* `Fullscreen on device display` ON
* `Force Landscape orientation` ON
* `Hide display cutout` ON
* `Show additional keyboard` OFF
* `Prefer scancodes when possible` ON
## Sterowanie
Dla kontrolera dotykowego aplikacja Input Bridge jest wymagana
## Odinstalowywanie
Aby odinstalować mobox, użyj `Backup and restore`.
## Debugowanie
Aby włączyć logging, wybierz opcję 2 w Mobox -> Settings -> Debug settings menu.

## Wsparcie
### Android
* `Android 10` lub wyżej jest rekomendowany.
### Urządzenie
* Większość telefonów z Androidem jest w stanie uruchomić `mobox` oraz gry DirectX9 korzystając z Mesa VirGL.
* Urządzenia ze Snapdragonem oraz Adreno 6xx lub Adreno 725-740 są rekomendowane aby uzyskać najlepszą kompatybilność i wydajność korzystając z Turnip+DXVK.
### Root
* Root nie jest wymagany.

## Znane problemy
* Jeżeli termux crashuje w momencie wejścia do menu, usuń dodatkowe skrypty motywu:
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* Niektóre urządzenia mogą zawieszać się w momencie tworzenia prefixu oraz instalacji PhysX, w takim wypadku zmień konfigurację w `Compatibility settings`

## Wesprzyj mobox
[boosty](https://boosty.to/olegos/donate)

#
Wielkie dzięki dla Hugo, JeezDisReez, ptitSeb, MishkaKolos, Xanzo, Jotaros, Maxython i innym za pomoc.

[MishkaKolos Discord](https://discord.gg/ZAQnZzbCXq)


## Wykorzystane aplikacje

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
