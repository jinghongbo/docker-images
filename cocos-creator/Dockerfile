FROM node as build
ADD https://storage.googleapis.com/otsimobuilds/cocos-creator-1.9.0-linux.tar.xz ./opt/
RUN tar xvjf cocos-creator-1.9.0-linux.tar.xz -d /opt/cocos-creator
RUN sh /opt/cocos-build.sh --path . --build "platform=web-mobile"