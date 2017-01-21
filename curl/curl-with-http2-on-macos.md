# Use curl with HTTP/2 on macOS

If you'll try to run `curl` with `--http2` flag with `curl` shipped with macOS by default (as of macOS 10.12) you'll get the following error:

```curl: (1) Unsupported protocol```

To fix that you can reinstall `curl` using brew with `--with-nghttp2` flag:

```brew install curl --with-nghttp2```

To replace standard `curl` with newly installed run:

```brew link curl --force```

and restart your terminal.
