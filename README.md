# Development Setup

This repository contains notes and instructions for installing and configuring basic development tools based on my personal preferences. The tools included in this repository are meant to serve as a starting point for setting up a development workstation and can be customized to suit your individual needs.

## Font

Download and install ***JetBrainsMono nerdfont***

```bash
curl -L -o ~/Downloads/fonts/nerdfont.zip --create-dirs \
    https://github.com/ryanoasis/nerd-fonts/releases/download/v2.2.2/JetBrainsMono.zip

unzip ~/Downloads/fonts/nerdfont.zip

sudo cp ~/Downloads/fonts/*.ttf /usr/share/fonts/truetype/

rm -drf ~/Downloads/fonts
```

Select this font in applications such as ***Terminal*** or ***Visual Studio Code***

## Shell

### Zsh

```bash
sudo apt install zsh

zsh --version
#zsh 5.9 (x86_64-ubuntu-linux-gnu)
```

Set as default shell

```bash
# Run Zsh and check which zsh is running
zsh
# Followed by
echo $SHELL

# Set Zsh as default
chsh -s $(which zsh)
```

Log out and back in, test default shell

```bash
echo $SHELL
#/usr/bin/zsh
```

### Oh my zsh

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Starship

Installation

```bash
curl -sS https://starship.rs/install.sh | sh
```

Setup ***Zsh*** to use ***Starship***

```bash
echo 'eval "$(starship init zsh)"' >> ~/.zshrc
```

Copy configuration file

```bash
cp ./assets/starship.toml ~/.config/starship.toml
```
