# dotfiles

This repository contains dotfiles for Ubuntu

## Prerequisites

Install `build-essential`

```bash
sudo apt install build-essential
```

Install `git`

```bash
sudo apt install git
```

## Installation

Clone the repository

```bash
git clone https://github.com/jaybarbhaiya/dotfiles.git ~/.dotfiles
```

Navigate to the repository

```bash
cd ~/.dotfiles
```

Fetch the git submodules (required to fetch the nvim configuration)

```bash
git submodule update --init
```

Install `homebrew` (required to install `neovim`)
Follow the instructions at [https://brew.sh/](https://brew.sh/)

## Linking files

```bash
sudo ln -s ~/.dotfiles/.bashrc ~/.bashrc
```

## Linking directories

```bash
sudo ln -s -r ~/.dotfiles/.config/nvim ~/.config/nvim
```

## List of tools installed by `homebrew`

```bash
brew bundle dump --describe
```

The above command dumps a file called `Brewfile`
which contains the list of tools installed by `homebrew`

## Installing tools from `Brewfile`

```bash
brew bundle --file ~/.dotfiles/Brewfile
```
