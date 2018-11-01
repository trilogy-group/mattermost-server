FROM docker:stable-dind

RUN sed -i -e 's/v[[:digit:]]\.[[:digit:]]/edge/g' /etc/apk/repositories
RUN apk update && apk upgrade --update-cache --available && apk add bash bash-completion go make git curl build-base nodejs npm procps

WORKDIR "/root/go/src/github.com/mattermost/mattermost-server"