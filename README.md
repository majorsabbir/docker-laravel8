# Introduction
This is a fresh laravel8 project with livewire and blade stack.

# Installation

Run the following command

```
git clone https://github.com/majorsabbir/docker-laravel8.git
cd docker-laravel8
docker-compose --build
docker-compose up -d
```

update .env
```
DB_HOST=mariadb
REDIS_HOST=redis
```
Note: ```mariadb``` and ```redis``` the service name mentioned in ```docker-compose.yml``` on line 46 and 65 respectively

## SSL Certificate

### Install MKCERT
```
sudo apt-get update && upgrade
sudo apt-get install libnss3-tool -y
wget https://github.com/FiloSottile/mkcert/releases/download/v1.4.1/mkcert-v1.4.1-linux-amd64
mv mkcert-v1.4.1-linux-amd64 mkcert
chmod +x mkcert
cp mkcert /usr/local/bin/
```

### Create SSL Certificate
```
cd .docker/nginx/ssl
sudo mkcert example.com '*.example.com' localhost 127.0.0.1
```

Note: rename certificate to ```cert.pem``` and key to ```cert-ket.pem```


## PHPMYADMIN
In order to access phpmyadmin ```http://localhost:7000```

## Application
```https://localhost```, ```https://127.0.0.1```, ```https://example.com```