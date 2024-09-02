## Create workspace directory

```sh
mkdir -p ~/workspace/tagpro
cd ~/workspace/tagpro
```

## Clone the repository

```sh
git clone https://github.com/tagpro/local-remote.git
cd local-remote/rasp-router-1/pihole
```

## Setup secrets for pihole

ssh to the machine and run the following command
```sh
# Assuming your current directory is where docker-compose is located
echo "PIHOLE PASSWORD" > pihole_password.txt
```
