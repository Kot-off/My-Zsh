#My ZSH
##Создадим скрипт app-install.sh и передадим туда следующие строки
```console
app = ["fira-code-fonts", "git", "curl", "bat", "duf", "exa", "fd", "tldr", "btop", "ncdu", "gping",]
sudo apt update -y
sudo apt install -y "${apps[@]}"
```

## Нужный шрифт - FiraCode NF
```console
https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode
```

## Команда для установки
```console
https://github.com/tonsky/FiraCode/wiki/Linux-instructions#installing-with-a-package-manager
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/FiraCode.zip
````

## Установите пакет ZSH

## ARCH ----->[<img src="https://cdn0.iconfinder.com/data/icons/flat-round-system/512/archlinux-512.png" width="50" height="50" >](https://archlinux.org/download/)
```console
sudo pacman -Sy zsh zsh-completions
````

## UBUNTU -->[<img src="https://brandslogos.com/wp-content/uploads/images/large/ubuntu-logo.png" width="50" height="50" >](https://ubuntu.com/)
```console
sudo apt -y install zsh
```

## FEDORA --->[<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Fedora_logo.svg/1024px-Fedora_logo.svg.png" width="50" height="50" >](https://getfedora.org/)
```console
sudo apt install zsh
```

## Установить ZSH по умолчанию
```console
sudo chsh -s /bin/zsh
```

## После переходим к настройкам
### Install Oh My Zsh
```console
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## Install PowerLevel10k
```console
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

## Установка темы
```console
sudo nano ~/.zshrc
```
```console
ZSH_THEME="powerlevel10k/powerlevel10k"
```

## Если после перезагрузки настройки не включились автоматически введите команду
```console
p10k configure
```

## Далее неоходимо раскоментировать некоторые параметры
```
nano .p10k.zsh
```

## Перезазапускаем файл, чтобы настройки сохранились
```
source .p10k.zsh
```

## Плагины

### Подсветка синтаксиса
```console
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

## Авто дополнение
```console
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## Включаем плагины
```console
sudo nano ~/.zshrc
```
```console
plugins=( git zsh-syntax-highlighting zsh-autosuggestions )
```

## Замена стандартных команд

### ls - установите пакет `exa`
```console
apt -y install exa
```

##откройте настройки шэла
```console
sudo nano ~/.zshrc
```

##добавьте в самый низ эти строки
```console
bash
if [ -x "$(command -v exa)" ]; then
    alias ls="exa --long --all --group"
fi
```

## cat - установите пакет `bat`
```console
sudo nano ~/.zshrc
```

##добавьте в самый низ эти строки
```console
alias cat="batcat"
```

## df - установите пакет `duf`
```console
sudo nano ~/.zshrc
```

добавьте в самый низ эти строки
```console
alias df="duf"
```

## find - установите пакет `fd`
```console
sudo nano ~/.zshrc
```
```console
alias find="fd"
```

## man - установите пакет `tldr`
```console
sudo nano ~/.zshrc
```
```console
alias man="tldr"
```
```
mkdir -p ~root/.local/share
tldr --update
```

## top - установите пакет `btop`
```console
sudo nano ~/.zshrc
```
```console
alias top="btop"
```

## du - установите пакет `ncdu`
```console
sudo nano ~/.zshrc
```
```console
alias du="ncdu"
```

## ping - установите пакет `gping`
```console
snap install gping
```
```console
sudo nano ~/.zshrc
```
```console
alias ping="gping"
```

## Включить подсветку в `nano`
```console
nano ~/.nanorc
```
```console
include /usr/share/nano/*.nanorc
```

# Плагины [OHMYZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins)


