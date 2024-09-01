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

## Setup secrets for pihole

ssh to the machine and run the following command
```sh
# Assuming your current directory is where docker-compose is located
echo "PIHOLE PASSWORD" > pihole_password.txt
```

## CloudFlare setup
```sh
# Get API token from https://dash.cloudflare.com/profile/api-tokens with `Zone:Read, DNS:Edit` permissions
nvim cf_api_token.txt

# Paste and then press `:wq`

# OR

echo "YOUR API TOKEN" > cf_api_token.txt
```

## Setup traefik data directory

```sh
cd data
touch acme.json
chmod 600 acme.json
```
## Setup docker proxy

```sh
docker network create proxy
```

## Create username and password for traefik dashboard

```sh
# Replace `user` with your username
echo $(htpasswd -nB user) | sed -e s/\\$/\\$\\$/g
```

## Put the output in .env file

```sh
nvim .env

# Add/update the following lines
TRAEFIK_DASHBOARD_CREDENTIALS="<Your output from above>"
```

## Update the data/traefik.yml file

Fix `TODO` in the file

## Update docker-compose.yml file

```sh
# Replace local.example.com with your domain
```


## Start the services

```sh
docker compose up -d
```
