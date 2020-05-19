FROM alpine:3.10.1


RUN apk add --update \
    curl \
    bash \
    && rm -rf /var/cache/apk/*

COPY getconfig.sh scripts/
RUN curl -Lso scripts/getconfig.php https://raw.githubusercontent.com/drydockcloud/tools-php-getconfig/master/getconfig.php

ENTRYPOINT [ "scripts/getconfig.sh" ]
