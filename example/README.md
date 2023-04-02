```sh
$ docker compose up
```

```sh
$ curl -H "Accept-Encoding: br" -I http://127.0.0.1
HTTP/1.1 200 OK
Server: nginx/1.23.4
Date: Sun, 02 Apr 2023 14:11:54 GMT
Content-Type: text/html
Last-Modified: Sun, 02 Apr 2023 13:22:13 GMT
Connection: keep-alive
ETag: W/"64298185-42"
Content-Encoding: br
```

I see `Content-Encoding: br` then Brotli compression is enabled.

More info, see https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Encoding

```sh
$ curl  -H "Accept-Encoding: gzip" -I http://127.0.0.1
HTTP/1.1 200 OK
Server: nginx/1.23.4
Date: Sun, 02 Apr 2023 14:19:19 GMT
Content-Type: text/html
Last-Modified: Sun, 02 Apr 2023 13:22:13 GMT
Connection: keep-alive
ETag: W/"64298185-42"
Content-Encoding: gzip
```
