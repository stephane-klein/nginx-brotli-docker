Ressources:

- https://github.com/google/ngx_brotli
- https://github.com/nginxinc/docker-nginx/tree/master/modules

```sh
$ docker build --build-arg ENABLED_MODULES="brotli" -t stephaneklein/nginx-brotli:1.23.4 .
```
