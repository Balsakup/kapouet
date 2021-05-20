# Kapouet

> Un starter pour les développer tous.  
> Un starter pour tout simplifier.  
> Un starter pour les déployer tous et dans le web les consulter

# Prérequis
- Docker
- Docker Compose
- NodeJS
- Yarn

# Installation
```shell
docker run --rm \
    -v $(pwd):/app \
    composer create-project --prefer-dist balsakup/composer <mon_site> 
```

```shell
cd <mon_site>
```

```shell
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/opt \
    -w /opt \
    laravelsail/php80-composer:latest \
    composer install --ignore-platform-reqs
```

```shell
./vendor/bin/sail up -d
```

L'application est maintenant accessible à l'adresse `http://localhost`
