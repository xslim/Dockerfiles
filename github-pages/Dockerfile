# FROM ruby:2.7.3-alpine

# RUN gem install bundler github-pages

# ENV LANG en_US.UTF-8
# ENV LANGUAGE en_US.UTF-8
# ENV LC_ALL en_US.UTF-8

# WORKDIR /src/site

# CMD ["jekyll", "serve", "-H", "0.0.0.0", "-P", "4000"]

# FROM alpine:edge

# RUN apk add --no-cache 
# RUN apk add --no-cache ruby nodejs npm yarn
# RUN apk add --no-cache ruby-bundler ruby-dev
# RUN apk add --no-cache jekyll=3.8.6
# RUN gem install github-pages

FROM ruby:2.7.1-alpine

ENV GITHUB_PAGES_VERSION 215

RUN apk add --no-cache --virtual .build_deps \
    make build-base && \
  gem install github-pages -v "$GITHUB_PAGES_VERSION" && \
  gem install jekyll-default-layout jekyll-sitemap jekyll-paginate jekyll-feed jekyll-seo-tag jekyll-redirect-from jekyll-sass-converter jekyll-avatar jekyll-github-metadata jekyll-optional-front-matter jekyll-remote-theme && \
  apk del .build_deps

RUN apk add --no-cache nodejs npm yarn

ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8
ENV LC_ALL en_US.UTF-8

WORKDIR /src/site
EXPOSE 4000 35729

CMD ["jekyll", "serve", "-H", "0.0.0.0", "-P", "4000", "--livereload"]
