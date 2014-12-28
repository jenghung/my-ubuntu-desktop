My Ubuntu Desktop
===
<img src="https://raw.githubusercontent.com/jenghung/my-ubuntu-desktop/master/screenshots/screenshot1.png">

<img src="https://raw.githubusercontent.com/jenghung/my-ubuntu-desktop/master/screenshots/screenshot2.png">

## Basic Install And Settings
### Install 
* vim, git, screen

### Settings
* .bashrc
```sh
alias ls='ls -a --color=auto'
alias rm='rm -i'
```
* /etc/screenrc
```sh
hardstatus alwayslastline " %-Lw%{= Bw}%n%f %t%{-}%+Lw %=| %0c:%s "
termcapinfo xterm* ti@:te@
#support color 256
attrcolor b ".I"    # allow bold colors - necessary for some reason
termcapinfo xterm 'Co#256:AB=\E[48;5;%dm:AF=\E[38;5;%dm' # tell screen how to set colors. AB = background, AF=foreground
defbce on    # use current bg color for erased chars
```

## Chinese Input
http://lodour.blogspot.tw/2014/08/ubuntu.html

## Brightness Fn Shortcut
http://askubuntu.com/questions/230609/brightness-keyboard-buttons-do-not-work-on-asus-1225c

## Fonts
http://scar.simcz.tw/article/2014/04/22/fix-ubuntu-14-04-lts-zh-font-selector/

http://ingramchen.io/blog/2014/07/ubuntu-noto-font.html

http://samwhelp.github.io/blog/read/linux/ubuntu/font/font-noto/

https://github.com/adobe-fonts

## Ubuntu yosemite Theme
http://www.noobslab.com/2014/11/mbuntu-macbuntu-1410-transformation.html

http://www.noobslab.com/2014/04/macbuntu-1404-pack-is-released.html

http://jamyy.us.to/blog/2014/12/6917.html

http://dgk15.deviantart.com/art/OS-X-Yosemite-theme-0-2-for-Ubuntu-14-04-472626539

https://www.youtube.com/watch?v=hh3x4loZPCw

https://www.youtube.com/watch?v=DSf7aujD7tI

http://andrewjhazelton.deviantart.com/art/OS-X-10-10-Yosemite-Wallpaper-Blur-458548536

## Icon
https://numixproject.org/

https://github.com/numixproject/numix-icon-theme-circle

## Solarized Color Theme
https://github.com/Anthony25/gnome-terminal-colors-solarized

https://github.com/seebi/dircolors-solarized

https://gist.github.com/gmodarelli/5942850

https://github.com/mattcan/solarized-gedit

## GIT
```sh
sudo apt get install gitg
sudo apt get install meld
```
http://www.gitguys.com/topics/merging-with-a-gui/?lang=zh

## JAVA Development Environment
http://www.webupd8.org/2012/01/install-oracle-java-jdk-7-in-ubuntu-via.html

plugin: jrebel, quick serach, eclipse color theme, easy shell

server: Jboss AS Tools

http://askubuntu.com/questions/156910/how-to-change-eclipse-font-sizes
