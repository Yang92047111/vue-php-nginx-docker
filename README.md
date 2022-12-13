# Vue x PHP x Nginx x Docker Compose

## Describe

This template is a example for an application using Vue and PHP.

The server uses Nginx and builds them on the Docker. 

## Template structure

| Location                 |  Content                                   |
|--------------------------|--------------------------------------------|
| `/nginx/`                | Nginx server & Nginx config.               |
| `/nginx/log/`            | Nginx action log.                          |
| `/php/`                  | PHP project & PHP config.                  |
| `/php/index.php`         | RESTful API entry points.                  |
| `/php/Controller/Api/`   | RESTful API with PHP.                      |
| `/php/inc/`              | PHP config & DB config.                    |
| `/php/Model/`            | Access Database action & SQL select.       |
| `/php/public/`           | Build from Vue in static assets.           |
| `/php/SQL/`              | DB SQL.                                    |
| `/vue/src/`              | Vue App.                                   |
| `/vue/src/main.js`       | JS application entry point.                |
| `/vue/public/index.html` | Html application entry point.              |
| `/vue/public/static/`    | Static assets.                             |
| `/vue/dist/`             | Bundled Assets Output (generated at `yarn build`) |

## Include

### Docker official image

| Images  |  Tag    |
|---------|---------|
| `nginx` | stable  |
| `php`   | 8.1-fpm |
| `node`  | 18.10   |

### Depend

* Vue CLI 3
* Vue Router
* Vuex
## Usage

```
git clone https://github.com/Yang92047111/vue-php-nginx-docker.git

cd vue-php-nginx-docker

docker-compose up -d
```

## Setting

In the docker-compose.yml file we need to setting the config for the multi-container.

```
services: 
    container name:
        build: folder where the Dockerfile from
        ports:
            - host port : container port
        volumes:
            - local path : container path
```

Dockerfile sets which image we build the container and initialize command.

```
# Image
FROM image : tag

# Initialize like
RUN apt-get update
```

## Future work

* Add the DB container.
* Find some interesting packages to include it.

## References