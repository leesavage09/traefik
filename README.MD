# startup script

## download repo

cd /home/dev
git clone https://github.com/leesavage09/traefik.git

## setup acme permissions

cd traefik/
chmod 600 ./certs/acme.json

## create a new basic auth password file

sudo htpasswd -c htpasswd admin

## setup .env file

cp sample.env .env
nano .env

## start traefik

docker-compose up -d
