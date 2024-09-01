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

## Install Apache2 Utils

```sh
sudo apt install apache2-utils -y
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
sudo chmod 660 /var/run/docker.sock # might fix permission issues
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

Uncomment the following line in `~/.zshrc` (should be at the top of the file):

```sh
export PATH=$HOME/bin:$HOME/.local/bin:/usr/local/bin:$PATH
```

## Setup [zoxide](https://github.com/ajeetdsouza/zoxide) and [fzf](https://github.com/junegunn/fzf)

```sh
sudo apt install fzf -y
curl -sSfL https://raw.githubusercontent.com/ajeetdsouza/zoxide/main/install.sh | sh
```

Add the following to your `.zshrc` file:

```sh
eval "$(zoxide init zsh)"
# OR
echo 'eval "$(zoxide init zsh)"' >> ~/.zshrc
```

We will add fzf to oh-my-zsh plugin list

```sh
plugins=(
    git
    fzf
)
```

## Install Portainer (OPTIONAL)

```sh
docker volume create portainer_data
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```
