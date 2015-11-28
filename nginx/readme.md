# Building Docker Engine X Image

docker build -t nginx .

# Usage

## http

docker run -d -p 80:80 -v $PWD:/etc/nginx/sites-enabled nginx

## http & https

docker run -d -p 80:80 -p 443:443 -v $PWD:/etc/nginx/sites-enabled nginx


## override default nginx configuration

docker run -d -p 80:80 -v $PWD/foldername:/etc/nginx/sites-enabled nginx
 

