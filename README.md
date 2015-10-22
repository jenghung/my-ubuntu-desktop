My Ubuntu Desktop
===
<img src="https://raw.githubusercontent.com/jenghung/my-ubuntu-desktop/master/screenshots/screenshot1.png">

> More screenshots:
>
> https://plus.google.com/communities/112725216256580894446/stream/921e0ee8-fdd9-43ee-b6c5-355c4c1d8cff

## Basic Install And Settings
```sh
sudo apt-get update
sudo apt-get install vim 
sudo apt-get install git
sudo apt-get install unity-tweak-tool
```
### Settings
* .bashrc
```sh
alias ls='ls -a --color=auto' 
alias rm='rm -i'
```
* nautilus

<img src="https://raw.githubusercontent.com/jenghung/my-ubuntu-desktop/master/screenshots/nautilus-setting.png">

## Chinese Input
### fcitx
```sh
sudo apt-get install fcitx
sudo add-apt-repository ppa:fcitx-team/nightly
sudo apt-get update
sudo apt-get install fcitx-chewing
```
* Change default ibus to fcitx.

<img src="https://raw.githubusercontent.com/jenghung/my-ubuntu-desktop/master/screenshots/ibus-to-fcitx.png">

> References:
>
> http://lodour.blogspot.tw/2014/08/ubuntu.html

## Brightness Fn Shortcut
http://askubuntu.com/questions/230609/brightness-keyboard-buttons-do-not-work-on-asus-1225c

## Fonts
* Download [Google Noto Sans Font](https://www.google.com/get/noto/pkgs/Noto-hinted.zip)

* Download Adobe Source Pro Series Fonts: [SourceSerifPro](https://github.com/adobe-fonts/source-serif-pro/releases), [SourceSansPro](https://github.com/adobe-fonts/source-sans-pro/releases), [SourceCodePro](https://github.com/adobe-fonts/source-code-pro/releases).

* [InputFont](http://input.fontbureau.com/)

* Move to all .otf to *~/.fonts* directory.

<img src="https://raw.githubusercontent.com/jenghung/my-ubuntu-desktop/master/screenshots/fonts-directory.png">

* Edit *~/.config/fontconfig/fonts.conf*
```sh
<fontconfig>
  <match target="pattern">
    <test qual="any" name="family">
      <string>serif</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
      <string>SourceSerif Pro</string>
      <string>Noto Sans CJK TC</string>
      <string>Noto Sans CJK SC</string>
      <string>Noto Sans CJK JP</string>
      <string>Noto Sans CJK KR</string>
    </edit>
  </match> 
  <match target="pattern">
    <test qual="any" name="family">
      <string>sans-serif</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
      <string>SourceSans Pro</string>
      <string>Noto Sans CJK TC</string>
      <string>Noto Sans CJK SC</string>
      <string>Noto Sans CJK JP</string>
      <string>Noto Sans CJK KR</string>
    </edit>
  </match>
  <match target="pattern">
    <test qual="any" name="family">
      <string>monospace</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
      <string>SourceCode Pro</string>
      <string>Noto Sans CJK TC</string>
      <string>Noto Sans CJK SC</string>
      <string>Noto Sans CJK JP</string>
      <string>Noto Sans CJK KR</string>
    </edit>
  </match>
</fontconfig>
```

* reboot or execute the follow command:
```sh
sudo fc-cache -fv
```

* test the sequence of font loading:
```sh
fc-match -s sans-serif | more
```

> References:
> 
> http://scar.simcz.tw/article/2014/04/22/fix-ubuntu-14-04-lts-zh-font-selector/
> 
> http://ingramchen.io/blog/2014/07/ubuntu-noto-font.html
> 
> http://samwhelp.github.io/blog/read/linux/ubuntu/font/font-noto/
> 
> https://github.com/adobe-fonts

## Flat Design Theme (Choose One!)
### theme
* MacBuntu themes and icons
```sh
sudo add-apt-repository ppa:noobslab/themes
sudo apt-get update
sudo apt-get install mbuntu-y-ithemes-v4
sudo apt-get install mbuntu-y-icons-v4
```

* OS-X-Yosemite-theme
```sh
Download from http://dgk15.deviantart.com/art/OS-X-Yosemite-theme-0-2-for-Ubuntu-14-04-472626539
put OSX-Yosemite folder to /usr/share/themes 
```
* [Ultra Flat Yosemite theme](http://gnome-look.org/content/show.php/Ultra-flat-Yosemite?content=168521)

* [Ultra Flat theme](http://gnome-look.org/content/show.php/Ultra-Flat?content=167473)

* [Paper theme](http://snwh.org/paper/)

* [Royal Ubuntu theme](https://medium.com/@foxoman/royal-ubuntu-theme-40a635534e1)

### icons
https://github.com/numixproject/numix-icon-theme-circle

http://gnome-look.org/content/show.php/Ultra-Flat-Icons?content=167477

https://github.com/NitruxSA/flattr-icons

http://xenlism.github.io/wildfire/

<hr>

> References:
>
> http://www.noobslab.com/p/themes-icons.html
>
> http://www.noobslab.com/2014/11/mbuntu-macbuntu-1410-transformation.html
>
> http://www.noobslab.com/2014/04/macbuntu-1404-pack-is-released.html
> 
> http://jamyy.us.to/blog/2014/12/6917.html
>
> https://www.youtube.com/watch?v=hh3x4loZPCw
>
> https://www.youtube.com/watch?v=DSf7aujD7tI
>
> http://andrewjhazelton.deviantart.com/art/OS-X-10-10-Yosemite-Wallpaper-Blur-458548536

## Solarized Color Theme
https://github.com/Anthony25/gnome-terminal-colors-solarized

https://github.com/seebi/dircolors-solarized

https://gist.github.com/gmodarelli/5942850

https://github.com/mattcan/solarized-gedit (gedit)

https://github.com/altercation/vim-colors-solarized (vim, gvim)

```sh
# change gvim font size at .vimrc
if has('gui_running')
  set guifont=Ubuntu\ Mono\ 13
endif
```

## GIT
* git prompt
```sh
#git bash
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}
PS1="${debian_chroot:+($debian_chroot)}\u@\h:\w\$(parse_git_branch)$ "
```
* git gui tools
```sh
sudo apt-get install gitg
sudo apt-get install meld
sudo add-apt-repository ppa:rabbitvcs/ppa
sudo apt-get update
sudo apt-get install rabbitvcs-nautilus3
```

http://wiki.rabbitvcs.org/wiki/install/ubuntu

http://www.gitguys.com/topics/merging-with-a-gui/?lang=zh

https://groups.google.com/forum/#!topic/rabbitvcs/TH5asGgkC6g  (Use en_GB)

## JAVA Development Environment
http://www.webupd8.org/2012/01/install-oracle-java-jdk-7-in-ubuntu-via.html

plugin: jrebel, quick serach, eclipse color theme, easy shell

decompiler: JD-eclipse, Realignment for JD-Eclipse

http://jd.benow.ca/

http://sourceforge.net/projects/realignmentjd/files/

server: Jboss AS Tools

http://stackoverflow.com/questions/11805784/very-large-tabs-in-eclipse-panes-on-ubuntu

http://stackoverflow.com/questions/3124629/how-can-i-configure-the-font-size-for-the-tree-item-in-the-package-explorer-in-e

## Microsoft Office
### Lync
```sh
sudo apt-get install pidgin 
sudo apt-get install pidgin-sipe
```
Edit /etc/environment
```sh
export NSS_SSL_CBC_RANDOM_IV=0
```

http://nknu.net/ubuntu-14-04-exchange-configuration-thunderbird-pidgin/#pidgin

http://www.howtogeek.com/45932/how-to-disable-pidgin-notifications-in-ubuntu/

### Office
http://www.omgubuntu.co.uk/2014/07/run-microsoft-office-web-apps-ubuntu-desktop

### One Drive
http://www.omgubuntu.co.uk/2014/06/one-drive-ubuntu-integration

https://github.com/xybu/onedrive-d

## VitualBox
### USB
http://askubuntu.com/questions/25596/how-to-set-up-usb-for-virtualbox

Download [Oracle VM VirtualBox Extension Pack](https://www.virtualbox.org/wiki/Downloads)

### share folder
http://ubuntuforums.org/archive/index.php/t-1871552.html

```sh
sudo apt-get update
sudo apt-get install virtualbox-guest-additions-iso
```

### resolution
http://superuser.com/questions/495670/how-can-i-get-windows-8-and-virtualbox-to-use-my-full-screen

## Chrome
```sh
sudo vi /usr/share/applications/google-chrome.desktop
# 在 [Desktop Entry], [NewWindow Shortcut Group], [NewIncognito Shortcut Group] 底下插入
StartupWMClass=Google-chrome-stable
```
