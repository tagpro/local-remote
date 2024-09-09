An easy way to deploy is using sed to update your domain name

```bash
sed -i 's/example.com/yourdomain.com/g' compose.yml
```

Then you can deploy using docker compose

```bash
docker compose up -d
```
