# heroku-buildpack-webp-binaries

Forked from https://github.com/clhuang/heroku-buildpack-webp-binaries.

## Modifications

- Reviewed the buildpack and validated the libwebp URL.
  - (https://storage.googleapis.com/downloads.webmproject.org/releases/webp/index.html linked from https://developers.google.com/speed/webp/docs/precompiled)

## Description

Heroku buildpack that installs webp binaries (cwebp, dwebp) into a dyno slug.

Should allow imagemagick to encode/decode webp images.

Based off of https://github.com/mojodna/heroku-buildpack-jemalloc.
