![logo](docs/img/logo.png "logo")

<a href="https://github.com/olegos2/mobox/blob/main">English</a>
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
简体中文
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-es.md">Español</a>

##

`Mobox` 是一个旨在使用 [Box64](https://github.com/ptitSeb/box64) 和 [Wine](https://www.winehq.org/) 在 [Termux](https://github.com/termux/termux-app) 中运行 Windows x86 应用程序的项目。

# 安装
1. 安装 [Termux](https://f-droid.org/repo/com.termux_118.apk)、[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) 和 [Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk)。

2. 打开 termux 并粘贴以下命令

```bash
curl -s -o ~/x https://raw.githubusercontent.com/olegos2/mobox/main/install && . ~/x
```

3. 在 termux 中输入 `mobox`。

# 配置
## Wine
Wine 可以在 `Manage packages` 菜单中安装或卸载。
要选择 wine 容器，请使用主菜单中的选项 4。
Mesa VirGL、Turnip、Wine Mono 和 Gecko 可以在 Wine Start Menu 中安装。
## 设置
### Box86 和 Box64 动态编译变量
有两个可切换的菜单用于更改 mobox 设置菜单中的动态编译变量。
有关动态编译变量的更多信息，请参阅 [Box64 usage](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md) 和 [Box86 usage](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md)。
### 系统设置
要更改 wine 区域设置、dxvk hud 预设或 Turnip 设置，请使用 mobox 中的 `System settings` 菜单。
只有在无法自动检测到 x11 分辨率时才使用回退分辨率。
如果您有骁龙 8 Gen 1、8+ Gen 1、7+ Gen 2，请在 `System settings` 菜单中启用 `select a7xx flickering fix (TU_DEBUG)` 中的第二个选项。
### Root 设置
如果您有 root 权限，则可以使用 OOM 调整器，这在低内存时阻止 termux 被杀死很有用。
## Termux-X11 推荐设置
* `Display resolution mode` exact
* `Display resolution` 1280x720
* `Reseed Screen While Soft Keyboard is open` 关闭
* `Fullscreen on device display` 打开
* `Force Landscape orientation` 打开
* `Hide display cutout` 打开
* `Show additional keyboard` 关闭
* `Prefer scancodes when possible` 打开
## 控制
对于触摸控制，需要 Input Bridge 应用程序
## 卸载
要卸载 mobox，请使用 `Backup and restore` 菜单。
## 调试
要启用日志记录-在 Mobox -> 设置 -> 调试设置菜单中选择选项 2。日志路径为 /sdcard/mobox_log.txt

## 支持状态
### Android
* 建议使用 `Android 10` 或更高版本。
### 设备
* 大多数 Android 手机都可以运行 `mobox` 并使用 Mesa VirGL 运行 DirectX 9 游戏。
* 推荐使用带有 Adreno 6xx 或 Adreno 725-740 的 Snapdragon 设备，以获得最佳性能和与 Turnip+DXVK 兼容性。
### Root
* 不需要 Root 权限。

## 已知问题
* 如果尝试进入 mobox 菜单时 termux 应用程序崩溃，请删除自定义主题脚本：
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* 某些设备在安装 PhysX 时可能会遇到前缀创建冻结问题，在这种情况下，请在 `Compatibility settings` 菜单中更改设置
* 对于 SD845 设备，请在 `Compatibility settings` 菜单中禁用 dri3

## 支持 mobox
[boosty](https://boosty.to/olegos/donate)

#
特别感谢 Hugo、JeezDisReez、ptitSeb、MishkaKolos、Xanzo、Jotaros、Maxython 等人的帮助。

[MishkaKolos Discord](https://discord.gg/ZAQnZzbCXq)


## 第三方应用程序

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
