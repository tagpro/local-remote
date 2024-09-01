# Setting up a remote machine
> **Note:** Assuming ssh is setup in host machine and you are connected

## Connect to the machine using ssh in VS Code

This can be used to run commands and also to edit files in the remote machine

1. Install the Remote - SSH extension in VS Code
2. Press `Cmd + Shift + P` or `Ctrl + Shift +P` (Command pallete) and type `Remote-SSH: Connect to Host...`
3. Enter the ssh path `user@hostname` and press enter
4. Enter the password and press enter

## Update the system

```sh
sudo apt update
sudo apt upgrade -y
```

## Install git

```sh
sudo apt install git -y
```

## Install docker

```sh
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

## Add user to docker group

```sh
sudo usermod -aG docker $USER
```

## Install nmap

```sh
sudo apt install nmap -y
```

## Install jq

```sh
sudo apt install jq -y
```

## Install htop

```sh
sudo apt install htop -y
```

## Install tmux

```sh
sudo apt install tmux -y
```

## Install vim

```sh
sudo apt install neovim -y
```

## Install tree

```sh
sudo apt install tree -y
```

## Install zsh

```sh
sudo apt install zsh -y
```

## Install oh-my-zsh

```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
