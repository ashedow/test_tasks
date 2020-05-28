FROM debian

RUN apt-get update && apt-get install -u \
nginx \
 # don'f forget to clear cash
 && rm -rf /var/lib/apt/lists/*

EXPOSE 80

# move frequently modified layers to the end of file
copy .  /opt/


# Better use smalest base image
# Use tags and versions
FROM alpine:3.11.5 

# use --repository key and set versions
RUN apk add --no-cach nginx && mkdir -p /run/nginx