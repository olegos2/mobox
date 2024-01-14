"![logo](docs/img/logo.png "logo")

Português
<a href="https://github.com/olegos2/mobox/tree/main">English</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ru.md">Русский</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ptBR.md">Português Brasileiro</a>

##

`Mobox` é um projeto criado para executar aplicativos do Windows x86 no [Termux](https://github.com/termux/termux-app) usando [Box64](https://github.com/ptitSeb/box64) e [Wine](https://www.winehq.org/).

# Instalação
1. Instale
[Termux](https://f-droid.org/repo/com.termux_118.apk),
[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) e
[Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk).

2. Abra o termux e cole o comando

```bash
curl -s -o ~/x https://raw.githubusercontent.com/olegos2/mobox/main/install && . ~/x
```

3. Digite `mobox` no termux.

# Configuração
## Wine
O Wine pode ser instalado ou desinstalado no menu `Gerenciar pacotes`.
Para selecionar o contêiner do Wine, use a opção 4 no menu principal.
Mesa VirGL, Turnip, Wine Mono e Gecko podem ser instalados no Menu Iniciar do Wine.
## Configurações
### Variáveis dynarec do Box86 e Box64
Há dois menus alternáveis para alterar as variáveis dynarec no menu de configurações do mobox.
Para mais informações sobre variáveis dynarec, consulte [Uso do Box64](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md) e [Uso do Box86](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md)
### Configurações do sistema
Para alterar a localidade do Wine, a predefinição do hud do dxvk ou as configurações do Turnip, use o menu `Configurações do sistema` no mobox.
A resolução de fallback é usada somente quando a resolução x11 não pode ser detectada automaticamente.
Se você tiver Snapdragon 8 Gen 1, 8+ Gen 1, 7+ Gen 2, ative a segunda opção em `selecionar correção de oscilação a7xx (TU_DEBUG)` no menu `Configurações do sistema`.
### Configurações de root
Se você tiver root, poderá usar o OOM Adjuster, que é útil se o eliminador de memória baixa parar o termux.
## Preferências do Termux-X11
* `Modo de resolução de exibição` exato
* `Resolução de exibição` 1280x720
* `Reinicializar tela enquanto o teclado virtual estiver aberto` DESLIGADO
* `Tela cheia na exibição do dispositivo` LIGADO
* `Forçar orientação paisagem` LIGADO
* `Ocultar recorte de exibição` LIGADO
* `Mostrar teclado adicional` DESLIGADO
* `Preferir códigos de varredura quando possível` LIGADO
## Controles
Para controles de toque, o aplicativo Input Bridge é necessário
## Desinstalar
Para desinstalar o mobox, use o menu `Backup e restauração`.
## Depuração
Para habilitar o registro - selecione a opção 2 no menu Mobox -> Configurações -> Configurações de depuração. O caminho para o log é /sdcard/mobox_log.txt

## Status de suporte
### Android
* `Android 10` ou superior é recomendado.
### Dispositivo
* A maioria dos celulares Android pode executar `mobox` e jogos DirectX 9 usando Mesa VirGL.
* O dispositivo Snapdragon com Adreno 6xx ou Adreno 725-740 é recomendado para obter o melhor desempenho e compatibilidade com Turnip+DXVK.
### Root
* Root não é necessário.

## Problemas conhecidos
* Se o aplicativo termux travar ao tentar entrar no menu mobox, remova os scripts de tema personalizados:
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* Alguns dispositivos podem ter problemas de congelamento de criação de prefixo ao instalar o PhysX, neste caso, altere as configurações no menu `Configurações de compatibilidade`
* Para o dispositivo SD845, desative o dri3 no menu `Configurações de compatibilidade`

#
Muito obrigado a Hugo, JeezDisReez, ptitSeb, MishkaKolos, Xanzo, Jotaros, Maxython e outros pela ajuda.

[MishkaKolos Discord](https://discord.gg/ZAQnZzbCXq)


## Aplicativos de terceiros

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
"