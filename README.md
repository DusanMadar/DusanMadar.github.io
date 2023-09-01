Install build dependencies.

```
apk update && apk add --no-cache build-base gcc cmake
```

Credits: https://github.com/BillRaymond/my-jekyll-docker-website#step-7-build-the-jekyll-website

```
bundle init
bundle add github-pages -v 227
bundle add webrick
```

NOTE: use `gem list | grep github-pages` to find the version of locally
installed github-pages. It was "227" at the time of writing.

Follow steps listed at https://github.com/BillRaymond/my-jekyll-docker-website#step-7-build-the-jekyll-website


Build the page
```
bundle exec jekyll new --force --skip-bundle .
```

Run server
```
bundle exec jekyll serve --livereload --host 0.0.0.0

```
