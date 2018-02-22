# composer dockerized

Smaller composer image, based on newer package versions.

### tico/composer vs composer

* Used `alpine:edge` instead of `php:7-alpine3.7` as base image
* Removed following dependencies: `bash`, `mercurial`, `subversion`, `openssh`, `openssl` (php ext works with `libopenssl`, not `openssl` itself), `zlib-dev` (php ext installs it automatically), `curl` (php ext uses `libcurl`, not `curl` itself) and many more default unused packages from official php image
* Refactored `Dockerfile`
* Reduced image size
