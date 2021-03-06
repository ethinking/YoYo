## YoYo

A comment service that never disturbs reading.

### Usage

Place the following code where you'd like YoYo to load:

```
<div id="YoYo"></div>
<script src="https://yoyo.minghe.me/dist/v0.1/index.js"></script>
```

### Deploy your own YoYo

YoYo is running on VPS with docker currently, it's very easy to deploy one by yourself.

* Make docker and docker-compose ready on your host
  [docker](https://docs.docker.com/get-started/)
  [docker-compose](https://docs.docker.com/compose/install/)

* Customize your nginx.conf, the default nginx.conf in devops/nginx is totally prepared for my YoYo server, it's  nice example though, it also enable https.

* Build YoYo services docker images

```
  docker-compose -p yoyo -f devops/compose.yml build
```

* Start YoYo serices

```
  docker-compose -p yoyo -f devops/compose.yml up
```

Done!!!, Your YoYo API Server is running on: https://<your-domain>/v1/api, and your YoYo client JavaScript code is serving on: https://<your-domain>/dist/v0.1/index.js

### Development

* clone YoYo

```
git clone https://github.com/metrue/YoYo
```

* start YoYo API Server

```
cd YoYo/backend && npm run start
```

* start YoYo client

```
cd YoYo/client && npm run develop
```

then YoYo is running on https://localhost:8080


### Showcases

* [https://minghe.me](https://minghe.me)
* [https://asmalltalk.com](https://asmalltalk.com)

### LICENSE

MIT
