FROM iron/node

RUN apk update && apk upgrade

# If you have native dependencies, you'll need extra tools
RUN apk add --update make gcc g++ python

# Update NPM to latest version
RUN npm install -g npm@latest

# Add common NPM build packages
RUN npm install -g node-gyp

# If you had native dependencies you can now remove build tools
# RUN apk del make gcc g++ python
RUN rm -rf /tmp/*
RUN rm -rf /var/cache/apk/*
# RUN rm -rm /root/.npm /root/.node-gyp
