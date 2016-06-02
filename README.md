# Docker container for errbot
Both the existing errbot docker containers are a little buggy and complicated. This is my simplifed errbot docker container. It is tuned for the xmpp backend at present but shouldn't be too hard to get other backends working.

## What it does
* Bot runs under non-root user
* Bot exposes data and plugin directories as volumes
* Bot exposes core configuration variables as envrioment variables

## What it still needs to do
* Expose more as envrioment variables

