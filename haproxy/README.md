# Building Docker HA Proxy Image

docker build -t haproxy .

# Usage
 
docker run -d -p 80:80 haproxy

## override default haproxy configuration

docker run -d -p 80:80 -v $PWD/foldername:/haproxy-override haproxy
 
