FROM docker:stable-dind

RUN sed -i -e 's/v[[:digit:]]\.[[:digit:]]/edge/g' /etc/apk/repositories

RUN apk update && apk upgrade --update-cache --available && apk add bash bash-completion \
    go make git curl build-base libressl libressl-dev zlib zlib-dev 

RUN apk add nodejs npm procps python libpng-dev \
    autoconf automake file libtool nasm yarn
    #ruby-dev ruby-json libc-dev linux-headers
    #ca-certificates openssl ncurses \
    #coreutils python2 gcc g++ libgcc linux-headers \
    #grep util-linux binutils findutils

RUN npm set unsafe-perm true 

ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8

WORKDIR "/root/go/src/github.com/mattermost/mattermost-server"