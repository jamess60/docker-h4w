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


## Adding Custom Icons 
By default, the icons are baked into the npm app. By creating a 2nd docker mount and by manually restoring the included icons, we can add our own! 
1) Add a second bind mount in dockercompose.yml which is /your/path/etc/whatever:/app/frontend/image/icons
2) Git clone the [evert/h4w](https://github.com/evert/h4w) repository to somewhere such as /tmp
3) Move contents of h4w/frontend/image/icons to whatever path is your 2nd bind mount 
4) Optional but recommended for cleanliness/maintainability  - under the icons dir, create a subdir (eg: extraimgs)
5) Add your custom icons to the directory - they must be 32x32 PNG files. 
6) Reference your new icons within the home.json file 

I plan to include some of my own eventually to save you the leg work :) 


## Changelog
### Version 1.0
- Initial image
- Packages `evert/h4w` v0.1.0 (pushed on 25-05-2026)


## Acknowledgements
- Original project: [evert/h4w](https://github.com/evert/h4w)

