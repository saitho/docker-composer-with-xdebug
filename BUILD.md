# How to build Docker images

## Composer 1

### Build

```
docker build ./composer1 -t saitho/composer-with-xdebug:1-php7.4 --target php74
```

```
docker tag saitho/composer-with-xdebug:1-php7.4 saitho/composer-with-xdebug:1
```

### Verification

Should return a PHP 7.4 version, a Composer 1 version
`docker run saitho/composer-with-xdebug:1 php -v`
`docker run saitho/composer-with-xdebug:1 composer --version`

### Pushing

```
docker push saitho/composer-with-xdebug:1-php7.4
docker push saitho/composer-with-xdebug:1
```

## Composer 2

### Build

```
docker build ./composer2 -t saitho/composer-with-xdebug:2-php7.4 --target php74
docker build ./composer2 -t saitho/composer-with-xdebug:2-php7.2 --target php72
```

```
docker tag saitho/composer-with-xdebug:2-php7.4 saitho/composer-with-xdebug:2
```

### Verification

Should return a PHP 7.2 version, a Composer 2 version
`docker run saitho/composer-with-xdebug:2-php7.2 php -v`
`docker run saitho/composer-with-xdebug:2-php7.2 composer --version`

Should return a PHP 7.4 version
`docker run saitho/composer-with-xdebug:2-php7.4 php -v`
`docker run saitho/composer-with-xdebug:2-php7.4 composer --version`

### Pushing

```
docker push saitho/composer-with-xdebug:2-php7.4
docker push saitho/composer-with-xdebug:2-php7.2
docker push saitho/composer-with-xdebug:2
```