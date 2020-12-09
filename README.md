# heroku-buildpack-webp-binaries

Forked from https://github.com/clhuang/heroku-buildpack-webp-binaries.

**Warning**: Appears that this has to come after ruby/rails in the buildpack
order. Maybe it's polluting `PATH`? When putting it directly after the
imagemagick buildpack, the error we got was `Bundler::GemNotFound: Could not
find rake-13.0.1 in any of the sources`.

## Modifications

- Reviewed the buildpack and validated the libwebp URL.
  - (https://storage.googleapis.com/downloads.webmproject.org/releases/webp/index.html linked from https://developers.google.com/speed/webp/docs/precompiled)
- Updated libwebp to version 1.1.0

## Description

Heroku buildpack that installs webp binaries (cwebp, dwebp) into a dyno slug.

Should allow imagemagick to encode/decode webp images.

Based off of https://github.com/mojodna/heroku-buildpack-jemalloc.
