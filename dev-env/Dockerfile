FROM alpine

MAINTAINER Taras Kalapun <tkalapun@gmail.com>

RUN apk --no-cache add openssl openssh-client ca-certificates curl git bash tmux vim
RUN apk --no-cache add make tree jq gnupg

ENTRYPOINT ["bash"]
