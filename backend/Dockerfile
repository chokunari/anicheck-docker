FROM alpine:latest
WORKDIR /App
# 共通
#RUN apk update && \
RUN apk add --no-cache nodejs \ 
    curl \
    vim \
    git \
    npm && \
    npm update npm && \
# backend
    mkdir backend && \
    cd ./backend && \
    pwd && \
    npm init -y && \
    npm install --save express \
    pg \
    log4js \  
    date-utils \
    body-parser \
    cors \
    helmet \
    morgan \
    express-jwt \
    jwks-rsa && \
    #express-generatorはグローバルにインストールする必要あり。
    npm install -g express-generator && \
    git clone https://github.com/chokunari/DiveWorksBackend.git
ENTRYPOINT [ "sh","/App/backend/DiveWorksBackend/start_backend.sh" ]
EXPOSE 4000

