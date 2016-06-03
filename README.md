# Docker container for errbot
Both the existing errbot docker containers are a little buggy and complicated. This is my simplifed errbot docker container. It is tuned for the xmpp backend at present but shouldn't be too hard to get other backends working.

## What it does
* Bot runs under non-root user
* Bot exposes data and plugin directories as volumes
* Bot exposes core configuration variables as envrioment variables

## What it still needs to do
* Expose more as envrioment variables
* Use virtualenv rather than global install for errbot (makes plugin auto-dependencies magic easier)

## Envrioment Variables
* ERRBOT_USERNAME
* ERRBOT_PASSWORD
* ERRBOT_ADMINS

## Example usage
```
sudo docker run -e ERRBOT_USERNAME=err@example.com -e ERRBOT_PASSWORD=changeme -e ERRBOT_ADMINS=admin@example.com webpigeon/errbot
```

## Volumes
* /home/errbot -> config.py is here, but you should use envrioment variables rather than change this.
* /home/errbot/data -> data volume
* /home/errbot/plugins -> plugin volume
