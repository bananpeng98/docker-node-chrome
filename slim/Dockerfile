FROM node:carbon-slim@sha256:94512a7aa8e6cb1c9fa72b4e05902e7ced1a4312c3597718e5db67025136ff2e
LABEL maintainer "Eric Norman <eric.norman98@hotmail.se>"

ARG REFRESHED_AT
ENV REFRESHED_AT $REFRESHED_AT

RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -
RUN echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list
RUN apt-get update -qqy && apt-get -qqyy install \
    google-chrome-stable \
  && rm -rf /var/lib/apt/lists/*
