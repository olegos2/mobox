![logo](docs/img/logo.png "logo")

English
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
<a href="https://github.com/olegos2/mobox/blob/main/README-id.md">Bahasa Indonesia</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-es.md">Español</a>

##

`Mobox` adalah proyek yang dirancang untuk menjalankan aplikasi windows x86 di [Termux](https://github.com/termux/termux-app) menggunakan [Box64](https://github.com/ptitSeb/box64) dan [Wine](https://www.winehq.org/).

# Instalasi
1. Install
[Termux](https://f-droid.org/repo/com.termux_118.apk),
[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) and
[Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk).

2. Buka termux dan tempel perintah

```bash
curl -s -o ~/x https://raw.githubusercontent.com/olegos2/mobox/main/install && . ~/x
```

3. Ketik `mobox` di termux.

# Konfigurasi
## Wine
Wine dapat diinstal atau dihapus instalasinya di `Manage Packages` 
Untuk memilih container wine, gunakan opsi 4 di menu utama.
Mesa VirGL, Turnip, Wine Mono dan Gecko dapat diinstal di Wine Start Menu.
## Pengaturan
### Variabel dinarec Box86 dan Box64
Ada dua menu yang dapat dialihkan untuk mengubah variabel dynarec di menu pengaturan mobox.
Untuk informasi lebih lanjut tentang variabel dynarec, lihat [Penggunaan Box64](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md) dan [Penggunaan Box86](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md)
### Pengaturan sistem
Untuk mengubah lokal wine, preset dxvk hud, atau pengaturan Turnip, gunakan menu `System Settings` di mobox.
Resolusi cadangan hanya digunakan ketika resolusi x11 tidak dapat dideteksi secara otomatis.
Jika Anda memiliki Snapdragon 8 Gen 1, 8+ Gen 1, 7+ Gen 2, aktifkan opsi kedua di `select a7xx flickering fix (TU_DEBUG)` di menu `System settings`.
### Pengaturan root
Jika Anda memiliki root, Anda dapat menggunakan OOM Adjuster yang berguna jika pembunuh memori rendah menghentikan termux.
## Preferensi Termux-X11
* `Display resolution mode` exact
* `Display resolution` 1280x720
* `Reseed Screen While Soft Keyboard is open` OFF
* `Fullscreen on device display` ON
* `Force Landscape orientation` ON
* `Hide display cutout` ON
* `Show additional keyboard` OFF
* `Prefer scancodes when possible` ON
## Kontrol
Untuk kontrol sentuh, aplikasi Input Bridge diperlukan
## Uninstall
Untuk menghapus instalasi mobox, gunakan menu `Backup and Restore`.
## Men-debug
Untuk mengaktifkan logging - pilih opsi 2 di Mobox -> Settings -> Debug setting menu. Jalur ke log adalah /sdcard/mobox_log.txt

## Status dukungan
### Android
* `Android 10` atau lebih tinggi dianjurkan.
### Perangkat
* Kebanyakan ponsel Android dapat menjalankan game `mobox` dan DirectX 9 menggunakan Mesa VirGL.
* Perangkat Snapdragon dengan Adreno 6xx atau Adreno 725-740 direkomendasikan untuk mencapai performa dan kompatibilitas terbaik dengan Turnip+DXVK.
### Root
* Root tidak diperlukan

## Masalah Dikenal
* Jika aplikasi termux mogok saat mencoba masuk ke menu mobox, hapus skrip tema khusus:
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* Beberapa perangkat mungkin mengalami masalah pembekuan pembuatan awalan saat menginstal PhysX, dalam hal ini ubah pengaturan di menu `Compatibility settings`
* Untuk perangkat SD845, nonaktifkan dri3 di menu `Compatibility settings`

## Mendukung mobox
[boosty](https://boosty.to/olegos/donate)

#
Terima kasih banyak kepada Hugo, JeezDisReez, ptitSeb, MishkaKolos, Xanzo, Jotaros, Maxython dan lain lain atas bantuannya.

[MishkaKolos Discord](https://discord.gg/ZAQnZzbCXq)


## Aplikasi pihak ketiga

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

[Mesa-VirGL](https://github.com/alexvorxx/Mesa-VirGL
