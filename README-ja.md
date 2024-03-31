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
日本語

##

`Mobox` は [Box64](https://github.com/ptitSeb/box64) と [Wine](https://www.winehq.org/) を使って [Termux](https://github.com/termux/termux-app) で Windows x86 アプリケーションを実行するように設計されたプロジェクトです。

# インストール
1. インストール
[Termux](https://f-droid.org/repo/com.termux_118.apk),
[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) and
[Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk).

2. termuxを開き、コマンドを貼り付ける

```bash
curl -s -o ~/x https://raw.githubusercontent.com/olegos2/mobox/main/install && . ~/x
```

3. termux に `mobox` と入力。

# コンフィグ
## Wine
Wine は `Manage packages` メニューでインストールまたはアンインストールできる。
Wine コンテナを選択するには、メインメニューのオプション 4 を使ってください。
Mesa VirGL、Turnip、Wine Mono、Gecko は Wine Start Menu からインストールできます。
## 設定
### Box86 と Box64 の dynarec 変数
mobox 設定メニューには、dynarec 変数を変更するための 2 つの切り替え可能なメニューがあります。
dynarec 変数の詳細については、[Box64 の使い方](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md)および [Box86 の使い方](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md)を参照のこと
### システム設定
Wine ロケール、dxvk hud プリセット、Turnip の設定を変更するには、mobox の `System settings` メニューを使用してください。
フォールバック解像度は、x11 解像度が自動的に検出できなかった場合にのみ使用される。
Snapdragon 8 Gen 1、8+ Gen 1、7+ Gen 2 を使用している場合は、`System settings` メニューの `select a7xx flickering fix (TU_DEBUG)` を選択し、2 番目のオプションを有効にしてください。
### Root 設定
root があれば、OOM Adjuster を使うことができ、メモリ不足でtermuxが止まってしまったときに便利です。
## Termux-X11 preferences
* `Display resolution mode` exact
* `Display resolution` 1280x720
* `Reseed Screen While Soft Keyboard is open` OFF
* `Fullscreen on device display` ON
* `Force Landscape orientation` ON
* `Hide display cutout` ON
* `Show additional keyboard` OFF
* `Prefer scancodes when possible` ON
## 操作方法
タッチコントロールには Input Bridge アプリが必要
## アンインストール
mobox をアンインストールするには、`Backup and restore` メニューを使用する。
## デバッグ
ロギングを有効にするには、Mobox -> Settings -> Debug settings menu でオプション 2 を選択してください。ログへのパスは /sdcard/mobox_log.txt です。

## サポート状況
### Android
* `Android 10` 以上を推奨。
### デバイス
* ほとんどのアンドロイド携帯は、Mesa VirGL を使って `mobox` や DirectX 9 のゲームを動かすことができます。
* 最高のパフォーマンスと Turnip+DXVK との互換性を実現するには、Adreno 6xx または Adreno 725-740 を搭載した Snapdragon デバイスを推奨します。
### Root
* Root は不要。

## 既知の問題
* mobox メニューに入ろうとすると termux アプリがクラッシュする場合は、カスタムテーマスクリプトを削除してください:
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* 一部のデバイスでは、PhysX のインストール時にプレフィックス作成がフリーズする問題が発生する可能性があります、この場合、`Compatibility settings` メニューの設定を変更します
* SD845 デバイスの場合、`Compatibility settings` メニューで dri3 を無効にしてください

## mobox のサポート
[boosty](https://boosty.to/olegos/donate)

#
Hugo、JeezDisReez、ptitSeb、MishkaKolos、Xanzo、Jotaros、Maxython、その他多くの協力に感謝する。

[MishkaKolos Discord](https://discord.gg/ZAQnZzbCXq)


## サードパーティアプリ

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

