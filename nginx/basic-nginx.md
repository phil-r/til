# Basic nginx

## Create simple nginx config

Here is a simple config for a reverse proxy, it will take all requests coming to our server with a `Host` header `example.com` and proxy the to the local port `8080`:

```
server {
  listen 80;
  server_name example.com;
  location / {
    proxy_pass http://localhost:8080;
  }
}
```

Standard place to add configs is `/etc/nginx/sites-available`

So we can create it like this:

```bash
vi /etc/nginx/sites-available/example.com.conf
```

And copy the config from above!


## Enabling config

After creating a config in `/etc/nginx/sites-available` folder we should create a symlink to it from `/etc/nginx/sites-enabled`, like this:

```bash
ln -s /etc/nginx/sites-available/example.com.conf /etc/nginx/sites-enabled/example.com.conf
```

This will allow us to disable config without deleting it completely, modifying, commenting out, etc.

## Testing and reloading nginx

To test, run:

```bash
nginx -t
```

If everything is fine reload nginx using following command:

```bash
nginx -s reload
```
