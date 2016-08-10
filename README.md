# Alpine-php
###To run the dev environment:

*SSH*

     u: root 
     p: root

*Run*

     docker run -it -v $PWD:/app -p 2244:22 -p 9000:9000 danielous/alpine-php:7-dev
 
###Using docker Compose

    version: '2'
    services:
      fpm:
          image: danielous/alpine-php:7-dev
          ports:
            - "2244:22"
            - "9000:9000"
          volumes:
            - "$PWD:/app"
