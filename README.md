# Docker nginx container with GeoIP database

This is a Docker nginx container that includes the MaxMind GeoIP Country database. It injects the X-Origin-Country-Core and X-Origin-Country-Name headers into http requests to the backend with the country code of the requester.

The comments in the Dockerfile should explain it all.

## Disclaimer

This product includes GeoLite2 data created by MaxMind, available from
<a href="http://www.maxmind.com">http://www.maxmind.com</a>.
