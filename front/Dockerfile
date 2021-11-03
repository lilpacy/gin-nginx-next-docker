FROM node:latest

WORKDIR /app

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo
ENV HOST 0.0.0.0

ADD package.json /app/package.json
ADD yarn.lock /app/yarn-lock

RUN apt-get update -y && \
  apt-get upgrade -y

ADD . /app

RUN yarn
RUN yarn install
RUN yarn build
# RUN yarn generate

EXPOSE 3000

CMD ["yarn", "start"]
