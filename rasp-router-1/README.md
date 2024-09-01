## Create workspace directory

```sh
mkdir -p ~/workspace/tagpro
cd ~/workspace/tagpro
```

## Clone the repository

```sh
git clone https://github.com/tagpro/local-remote.git
cd local-remote/rasp-router-1
```

## Setup secrets password

ssh to the machine and run the following command
```sh
# Assuming your current directory is where docker-compose is located
echo "PIHOLE PASSWORD" > pihole_password.txt
echo "CLOUDFLARE API KEY" > cf_api_token.txt
```

## Setup traefik data directory

```sh
mkdir -p data && cd data
touch acme.json
chmod 600 acme.json
```

## Start the services

```sh
docker compose up -d
```

