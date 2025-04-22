# [Choice] Ruby version (use -bullseye variants on local arm64/Apple Silicon): 3, 3.3, 3.2, 3.1, 3.0, 3-bookworm, 3.3-bookworm, 3.2-bookworm, 3.1-bookworm, 3-bullseye, 3.3-bullseye, 3.2-bullseye, 3.1-bullseye, 3.0-bullseye, 3-buster, 3.2-buster 3.1-buster, 3.0-buster
ARG VARIANT=3.3.0-bookworm
FROM ruby:${VARIANT}

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt update && apt upgrade -y \
    && apt install -y --no-install-recommends libvips sqlite3 libsqlite3-dev nodejs yarn

RUN gem update --system
RUN gem install bundler
RUN gem install rails -v "~> 7.1.3"
RUN gem install foreman
