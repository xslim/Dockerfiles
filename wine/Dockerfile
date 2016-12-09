FROM alpine

MAINTAINER Taras Kalapun <tkalapun@gmail.com>

RUN apk --no-cache add wine

RUN ln -s /usr/bin/wine64 /usr/bin/wine

ENTRYPOINT ["wine"]
