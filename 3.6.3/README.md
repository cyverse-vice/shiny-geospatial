# shiny-geospatial
Shiny-Server with geospatial dependencies, based on [Rocker Shiny Docker container](https://hub.docker.com/r/rocker/shiny) for CyVerse VICE. VICE requires additional configuration files to be compatible with our Condor and Kubernetes orchestration.

[![CircleCI](https://circleci.com/gh/cyverse-vice/shiny-geospatial.svg?style=svg)](https://circleci.com/gh/cyverse-vice/shiny-geospatial) [![license](https://img.shields.io/badge/license-GPLv3-blue.svg)](https://opensource.org/licenses/GPL-3.0) [![Project Supported by CyVerse](https://img.shields.io/badge/Supported%20by-CyVerse-blue.svg)](https://www.cyverse.org) [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3246936.svg)](https://doi.org/10.5281/zenodo.3246936)

image | tag | size | metrics | build | 
----- | --- | ---- | ------- | ------|
[![DockerHub](https://img.shields.io/badge/DockerHub-brightgreen.svg?style=popout&logo=Docker)](https://hub.docker.com/r/cyversevice/shiny-geospatial) | [![](https://images.microbadger.com/badges/version/cyversevice/shiny-geospatial.svg)](https://microbadger.com/images/cyversevice/shiny-geospatial "latest") |  [![](https://images.microbadger.com/badges/image/cyversevice/shiny-geospatial.svg)](https://microbadger.com/images/cyversevice/shiny-geospatial "latest") | [![](https://img.shields.io/docker/pulls/cyversevice/shiny-geospatial.svg?label=pulls&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/shiny-geospatial)  |  [![](https://img.shields.io/docker/cloud/automated/cyversevice/shiny-geospatial.svg?label=build&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/shiny-geospatial/builds) 

launch | tag | size | metrics | build |
------ | ----| ---- | ------- | ------|
[![VICE](https://img.shields.io/badge/CyVerse-VICE-blue.svg?style=popout&logo=Docker&color=#1488C6)]()| [![](https://images.microbadger.com/badges/version/cyversevice/shiny-geospatial.svg)](https://microbadger.com/images/cyversevice/shiny-geospatial "latest") | [![](https://images.microbadger.com/badges/image/cyversevice/shiny-geospatial.svg)](https://microbadger.com/images/cyversevice/shiny-geospatial) | [![](https://img.shields.io/docker/pulls/cyversevice/shiny-geospatial.svg?label=pulls&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/shiny-geospatial) | [![](https://img.shields.io/docker/cloud/automated/cyversevice/shiny-geospatial.svg?label=build&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/shiny-geospatial/builds) 

# Instructions

## Run Docker locally or on a Virtual Machine

To run the Shiny-Server, you must first `pull` from DockerHub, or activate a [CyVerse Account](https://user.cyverse.org/services/mine) and launch in the Discovery Environment VICE.

```
docker pull cyversevice/shiny-geospatial:latest
```

```
docker run -it --rm -d -p 3838:3838 cyversevice/shiny-geospatial:latest
```

## Run Docker container in CyVerse VICE

Unless you plan on making changes to this container, you should just use the existing launch button above. 

###### Developer notes

To test the container locally:

```
docker run -it --rm -p 3838:3838 -e REDIRECT_URL=http://localhost:3838 cyversevice/shiny-geospatial:latest
```
