FROM alpine:latest
WORKDIR /App
# 共通
RUN apk update && \
    apk add --no-cache nodejs \ 
    curl \
    vim \
    git \
    npm && \
    npm update npm && \
# frontend
    npm install -g yarn cors-anywhere && \
    #プロジェクト名は全部小文字の必要あり。
    npx create-react-app anicheck-frontend && \
    cd anicheck-frontend && \
    pwd && \
    yarn add @material-ui/core \
    react-router \
    react-router-dom \
    axios \
    auth0-js \
    @material-ui/icons \
    react-swipeable-views \
    dotenv
#    git clone https://github.com/chokunari/DiveWorksFront.git
# ENTRYPOINT [ "sh","/App/frontend/diveworks/DiveWorksFront/start_front.sh" ]
EXPOSE 3000

