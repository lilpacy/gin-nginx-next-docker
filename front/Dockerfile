FROM node:latest

WORKDIR /app
COPY . /app

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

ENV NODE_OPTIONS --openssl-legacy-provider
# workaround to avoid webpack problem
# https://github.com/webpack/webpack/issues/14532
RUN yarn install

EXPOSE 3000

RUN chmod +x /app/start.sh
CMD ["/app/start.sh"]
