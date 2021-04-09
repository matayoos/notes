# My first steps on Ubuntu

## [Fabio_akita](https://www.youtube.com/watch?v=epiyExCyb2s&t=3754s)

### Tweaks tools
- $ sudo apt install gnome-tweak-tool

### Flat-remix theme
- mkdir 'get-started' && cd get-started
- https://www.osradar.com/install-flat-remix-theme-ubuntu/

### Ark-dark
- sudo apt-get install autoconf automake pkg-config libgtk-3-dev make
- ./autogen.sh --prefix=/usr --with-gnome=3.22
- User-themes extentions

### Tela-dark
- [github](https://github.com/vinceliuice/Tela-icon-theme)

### Vim
- sudo apt install vim-gtk3

### asdf

- https://asdf-vm.com/#/core-manage-asdf-vm
- That solve all my problems

- asdf plugin-list
- asdf list-all nodejs
- asdf install nodejs 12.19.0
- asdf global nodejs 12.19.0

- asdf local nodejs 12.19.0

> sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python-openssl git

## [Bruno_Germano](https://www.youtube.com/watch?v=W_AnWAiuzaw&t)

## [Diolinux]()

## Others usefull extensions

1. windowoverlay icon
1. Sound input & output device chooser
1. Auto move window
1. vitals
1. unite
1. Multi Monitors Add-On
1. openweather

## Matheus Goncalves

### Fish shell 

- https://github.com/fish-shell/fish-shell/
- sudo apt-add-repository ppa:fish-shell/release-3
- sudo apt-get update
- sudo apt-get install fish
- chsh -s /usr/bin/fish

> cd ~/.config/fish/
> touch config.fish
> source ~/.asdf/asdf.fish


### LAMP

- Enable ufw
  - sudo ufw enable
  - sudo ufw default deny
  - sudo iptables -L
- How To Find your Server’s Public IP Address
  - My network device logical name it not equals than the example, so I must
    found the right one;
  - Find the network device logical name command
    - sudo lshw -C network
  - ~~~bash ip addr show *enp1s0f1* | grep inet | awk '{ print $2; }' | sed
    's/\/.*$//'~~~
    - My ip: 192.168.0.18
