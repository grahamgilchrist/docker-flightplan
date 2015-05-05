FROM node:0.12

# Make sure we have rsync installed as well
RUN apt-get update && \
    apt-get install -y rsync && \
    rm -rf /var/lib/apt/lists/*

# Install the flightplan CLI tool globally
RUN npm install -g flightplan@0.6.2 \
    && npm cache clear
