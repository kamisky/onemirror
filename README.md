# OneMirror

[![](https://badge.imagelayers.io/bohan/onemirror:latest.svg)](https://imagelayers.io/?images=bohan/onemirror:latest 'Get your own badge on imagelayers.io')

OneMirror is a Docker image of Nginx. With already configured Google Search, Google Fonts and Gravatar proxy, it helps you to start your own mirror site easily.

## Info

 - Build parameters is from the offical Debian package
 - Latest mainline version Nginx
 - Latest stable OpenSSL
 - Google Search mirror module `ngx_http_google_filter_module` added
 - With Google Search, Google Fonts and Gravatar proxy configuration example

## Usage

### Basic HTTP Google mirror

    $ docker run -p 80:80 -d bohan/onemirror
    
### Custom configuration and SSL

 - You can use your own nginx.conf,
 - and your own site configuartions at nginx/conf.d,
 - and also enable SSL (Please read `nginx/ssl/README.txt`)
 - Build it 
 - `$ docker build -t mirror .`
 - and use it
 - `$ docker run -p 80:80 -d mirror`

## License

MIT
