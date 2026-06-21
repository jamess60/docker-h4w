# docker-h4w

A lightweight Docker deployment for [evert/h4w](https://github.com/evert/h4w).


## Changes to the Base Repo
- Removed evert's "my website" from the credits, as it points to a HomeAssistant instance.
- Included links to the GitRepo and Dockerhub page:
  - [Git Repository](https://github.com/jamess60/docker-h4w)
  - [Docker Hub Page](https://hub.docker.com/r/jamess60/docker-h4w)


## Installation
1) Clone this git repo to /tmp, move the dockercompose.yml to your directory of choice, and move the /data dir (later mapped as a volume) to your directory of choice
2) Edit the docker compose file to include your persistent volume mount (should map to the included data directory) and port of choice
3) Run the the included docker compose file
4) Edit the icons & URLs according to [Evert's instructions](https://github.com/evert/h4w/blob/main/README.md)




## Changelog
### Version 1.0
- Initial image
- Packages `evert/h4w` v0.1.0 (pushed on 25-05-2026)


## Acknowledgements
- Original project: [evert/h4w](https://github.com/evert/h4w)

