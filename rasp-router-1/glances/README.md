An easy way to deploy is using sed to update your domain name

```bash
sed -i 's/example.com/yourdomain.com/g' compose.yml
```

Then you can deploy using docker compose

```bash
docker compose up -d
```

Or, you can use portainer to deploy this as a stack.
Just copy the contents of `compose.yml` and paste it into the stack editor in portainer.
