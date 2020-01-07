*Breaking update 07/01/2020*

On 30/12/2019 [Maxmind changed their license of accessing the free gepip2 databases](https://dev.maxmind.com/geoip/geoip2/geolite2/#), breaking how this Docker image works. I might spend some time getting the new license key method working with this image, but for now this Dockerfile is broken.

# Docker nginx container with GeoIP database

This is a Docker nginx container that includes the MaxMind GeoIP Country database. It injects the X-Origin-Country-Code and X-Origin-Country-Name headers into http requests to the backend with the country code of the requester.

The comments in the Dockerfile should explain it all.

## A few comments how this Dockerfile works

This image uses a pretty poor way to build the geoip2 module, with hardcoding the whole build args, but it works just fine. Ideally you should build a better image for production use and only use this for development and testing purposes.

As of writing nginx 1.13 is an old, unsupported version, so you probably want to make a new version with the current mainline nginx.


## Disclaimer

This product includes GeoLite2 data created by MaxMind, available from
<a href="http://www.maxmind.com">http://www.maxmind.com</a>.
