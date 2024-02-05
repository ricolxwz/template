FROM node:20.11.0-alpine3.19
LABEL maintainer="wenzexu"
WORKDIR /app
ENV PATH /app/node_modules/.bin:$PATH
COPY package.json package-lock.json ./
RUN npm config set cache /app/.npm-cache --global && \
    npm install --silent && \
    adduser \
        -D \
        -H \
        wenzexu && \
    chown -R wenzexu:wenzexu /app
USER wenzexu