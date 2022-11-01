# cdn

nginx-powered CDN and image thumbnailer, proxied via Traefik.

Example: https://static.elecena.pl/thumb/a/8/5/a85c303a45cd7a6b3745cb9aaa6b4f19.jpg (cropped to 100x100 px)

### Local development

```
$ curl http://localhost:2020
Hello

$ curl -I http://localhost:2020/favicon.ico
HTTP/1.1 204 No Content
Date: Tue, 01 Nov 2022 16:18:16 GMT
Connection: keep-alive

$ curl -I http://localhost:2020/thumb/a/8/5/a85c303a45cd7a6b3745cb9aaa6b4f19.jpg
HTTP/1.1 200 OK
Date: Tue, 01 Nov 2022 16:18:26 GMT
Content-Type: image/jpeg
Content-Length: 3404
Connection: keep-alive
Last-Modified: Mon, 21 Jun 2021 21:37:06 GMT
ETag: W/"a85c303a45cd7a6b3745cb9aaa6b4f19"
Cache-Control: max-age=2592000
Expires: Thu, 01 Dec 2022 16:18:26 GMT
X-Cache-Status: HIT
Accept-Ranges: bytes
```
