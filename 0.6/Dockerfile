FROM node:0.12

# Make sure we have rsync installed as well
RUN apt-get update && \
    apt-get install -y rsync && \
    rm -rf /var/lib/apt/lists/*

# Install the flightplan CLI tool globally
RUN npm install -g flightplan@0.6.2 \
    && npm cache clear

# Make working directory for app source
RUN mkdir -p /usr/src/app
WORKDIR /usr/src

# Install the local flightplan module so we don't have to include per project
RUN npm install flightplan@0.6.2 \
    && npm cache clear

# Reset the workdir for the project
WORKDIR /usr/src/app
