FROM alpine

WORKDIR /usr/app

RUN apk add --no-cache git nodejs nodejs-npm && \
  git clone https://github.com/miahon/fullstack-osa3.git . && \
  npm install && \
  apk del git && \
  adduser -D app && \
  chown -R app /usr/app 

USER app

EXPOSE 30001
CMD ["npm","start"]



