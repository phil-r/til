# Use curl with HTTP/2 on macOS

If you'll try to run `curl` with `--http2` flag with `curl` shipped with macOS by default (as of macOS 10.12) you'll get the following error:

```bash
curl -I --http2 https://http2.akamai.com/
curl: (1) Unsupported protocol
```

To fix that you can reinstall `curl` using [brew](http://brew.sh/) with `--with-nghttp2` flag and replace the standard `curl` with newly installed:

```bash 
brew install curl --with-nghttp2
brew link curl --force
```

and after you restart your terminal:

```bash
curl -I --http2 https://http2.akamai.com/
HTTP/2 200
server: Apache
...
```
