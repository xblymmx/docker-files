# Intro

Runs ss and privoxy to bypass GFW.


## Usage
Edit example.json for proper configurations

```sh

docker-compose up -d

docker exe -it provoxy sh

vi /etc/privoxy/config

# edit this line
# forward-socks5t   /               127.0.0.1:9050 .       
forward-socks5t   /               ss:[port] .         

exit

docker-compose restart
```


## Test network status

```
http_proxy=http://127.0.0.1:8118 curl www.google.com
```