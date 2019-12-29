FROM node:13.5.0-alpine

RUN apk update && \
    apk add git && \
    apk add --no-cache curl && \
    curl -o- -L https://yarnpkg.com/install.sh | sh

ENV PATH $HOME/.yarn/bin:$HOME/.config/yarn/global/node_modules/.bin:$PATH

ENV CHOKIDAR_USEPOLLING=true
RUN yarn global add @vue/cli

EXPOSE 3000

CMD ["/bin/sh"]