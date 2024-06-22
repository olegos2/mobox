![logo](docs/img/logo.png "logo")

<a href="https://github.com/olegos2/mobox/tree/main">English</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ru.md">Русский</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ua.md">Українська</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pt_BR.md">Português Brasileiro</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pl.md">Polski</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ja.md">日本語</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-zh_CN.md">简体中文</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
Español

##

`Mobox` es un proyecto diseñado para ejecutar aplicaciones de Windows x86 en [Termux](https://github.com/termux/termux-app) utilizando [Box64](https://github.com/ptitSeb/box64) y [Wine](https://www.winehq.org/).

# Instalación
1. Instala
[Termux](https://f-droid.org/repo/com.termux_118.apk),
[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) e
[Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk).

2. Abre Termux y pega el siguiente comando:

```bash
curl -s -o ~/x https://raw.githubusercontent.com/olegos2/mobox/main/install && . ~/x
```

3. Escribe `mobox` en Termux.

# Configuración
## Wine
Wine se puede instalar o desinstalar en el menú `Manage packages`.
Para seleccionar el contenedor de Wine, utiliza la opción 4 en el menú principal.
Mesa VirGL, Turnip, Wine Mono y Gecko se pueden instalar en el menú de inicio de Wine.
## Configuración
### Variables dynarec de Box86 y Box64
Hay dos menús conmutables para cambiar las variables dynarec en el menú de configuración de Mobox.
Para más información sobre las variables dynarec, consulta [Box64 usage](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md) y [Box86 usage](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md).
### Configuración del sistema
Para cambiar la configuración regional de Wine, el preajuste de dxvk hud o la configuración de Turnip, utiliza el menú `System settings` en Mobox.
La resolución de reserva se utiliza solo cuando la resolución de x11 no se puede detectar automáticamente.
Si tienes un Snapdragon 8 Gen 1, 8+ Gen 1, 7+ Gen 2, habilita la segunda opción en `select a7xx flickering fix (TU_DEBUG)` en el menú `System settings`.
### Configuración de root
Si tienes root, puedes usar OOM Adjuster, que es útil si el killer de baja memoria detiene Termux.
## Preferencias de Termux-X11
* `Display resolution mode` exacto
* `Display resolution` 1280x720
* `Reseed Screen While Soft Keyboard is open` OFF
* `Fullscreen on device display` ON
* `Force Landscape orientation` ON
* `Hide display cutout` ON
* `Show additional keyboard` OFF
* `Prefer scancodes when possible` ON
## Controles
Para los controles táctiles, se requiere la aplicación Input Bridge.
## Desinstalar
Para desinstalar Mobox, utiliza el menú `Backup and restore`.
## Depuración
Para habilitar el registro, selecciona la opción 2 en Mobox -> Settings -> Debug settings menu. La ruta al registro es /sdcard/mobox_log.txt.

## Estado de soporte
### Android
* Se recomienda `Android 10` o superior.
### Dispositivo
* La mayoría de los teléfonos Android pueden ejecutar `mobox` y juegos DirectX 9 usando Mesa VirGL.
* Se recomienda un dispositivo Snapdragon con Adreno 6xx o Adreno 725-740 para lograr el mejor rendimiento y compatibilidad con Turnip+DXVK.
### Root
* No se requiere root.

## Problemas conocidos
* Si la aplicación Termux se cierra cuando intentas ingresar al menú de Mobox, elimina los scripts de temas personalizados:
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* Algunos dispositivos pueden tener problemas de congelación al crear el prefijo cuando se instala PhysX. En este caso, cambia la configuración en el menú `Compatibility settings`.
* Para el dispositivo SD845, deshabilita dri3 en el menú `Compatibility settings`.

## Apoya a Mobox
[boosty](https://boosty.to/olegos/donate)

#
Muchas gracias a Hugo, JeezDisReez, ptitSeb, MishkaKolos, Xanzo, Jotaros, Maxython y otros por su ayuda.

[Discord de MishkaKolos](https://discord.gg/ZAQnZzbCXq)

## Aplicaciones de terceros

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
