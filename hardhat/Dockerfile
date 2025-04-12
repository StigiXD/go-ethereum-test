# Support setting various labels on the final image
ARG COMMIT=""
ARG VERSION=""
ARG BUILDNUM=""

# Requires Nodejs
FROM node:22-alpine

WORKDIR /tmp/app

# Get dependencies - will also be cached if we won't change go.mod/go.sum
COPY . /tmp/app

RUN npm install --save-dev hardhat

EXPOSE 8545

# Add some metadata labels to help programmatic image consumption
ARG COMMIT=""
ARG VERSION=""
ARG BUILDNUM=""

LABEL commit="$COMMIT" version="$VERSION" buildnum="$BUILDNUM"
