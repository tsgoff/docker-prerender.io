FROM selenium/node-chrome

RUN sudo apt-get update && \
    sudo apt-get -y install git nodejs npm && \
    sudo mkdir -p /data && sudo chown seluser /data

WORKDIR /data

ADD server.js .

RUN npm install prerender

EXPOSE 3000
CMD [ "node", "server.js" ]
