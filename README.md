# Docker nginx container with GeoIP database

This is a Docker nginx container that includes the MaxMind GeoIP Country database. It injects the X-Origin-Country-Code and X-Origin-Country-Name headers into http requests to the backend with the country code of the requester.

The comments in the Dockerfile should explain it all.

## Important

*Update 28/10/2019*

  - This image uses a pretty poor way to build the geoip2 module, with hardcoding the whole build args, but it works just fine. Ideally you should build a better image production and only use this for development and testing purposes.
  - As of writing nginx 1.13 is an old, unsupported version, so you probably want to make a new version with the current mainline nginx.


## Disclaimer

This product includes GeoLite2 data created by MaxMind, available from
<a href="http://www.maxmind.com">http://www.maxmind.com</a>.
