[![Project Supported by CyVerse](https://img.shields.io/badge/Supported%20by-CyVerse-blue.svg)](https://learning.cyverse.org/projects/vice/en/latest/) [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3246936.svg)](https://doi.org/10.5281/zenodo.3246936) [![](https://images.microbadger.com/badges/license/cyversevice/shiny-geospatial.svg)](https://microbadger.com/images/cyversevice/shiny-geospatial)

# shiny-geospatial

Shiny-Server with geospatial dependencies, based on [Rocker Shiny Docker container](https://hub.docker.com/r/rocker/shiny) for CyVerse VICE. VICE requires additional configuration files to be compatible with our Condor and Kubernetes orchestration.

[![CircleCI](https://circleci.com/gh/cyverse-vice/shiny-geospatial.svg?style=svg)](https://circleci.com/gh/cyverse-vice/shiny-geospatial) [![DockerHub](https://img.shields.io/badge/DockerHub-brightgreen.svg?style=popout&logo=Docker)](https://hub.docker.com/r/cyversevice/shiny-geospatial)

quick launch | tag | size | metrics | build | status |  
------------ | --- | ---- | ------- | ------|--------|
<a href="https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=12889c80-f38d-4737-bc38-1cda6badce39&app-id=203b0bc2-e2a5-11e8-9df7-008cfa5ae621" target="_blank"><img src="https://de.cyverse.org/Powered-By-CyVerse-blue.svg"></a> | [![TAG](https://images.microbadger.com/badges/version/cyversevice/shiny-geospatial.svg)](https://microbadger.com/images/cyversevice/shiny-geospatial) | [![SIZE](https://images.microbadger.com/badges/image/cyversevice/shiny-geospatial.svg)](https://microbadger.com/images/cyversevice/shiny-geospatial) | [![Docker Pulls](https://img.shields.io/docker/pulls/cyversevice/shiny-geospatial?color=blue&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/shiny-geospatial) | [![Docker Automated Build](https://img.shields.io/docker/cloud/automated/cyversevice/shiny-geospatial.svg?label=build&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/shiny-geospatial/builds)  | [![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/cyversevice/shiny-geospatial?color=blue&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/shiny-geospatial) 

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

To build your own container with a Dockerfile and additional dependencies, pull the pre-built image from DockerHub:

```
FROM cyversevice/shiny-geospatial:latest
```

Shiny requires an application to be added to the tool before it is run. You can add your shiny app installation when the container is built, 

Follow the instructions in the [VICE manual for integrating your own tools and apps](https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/developer_guide/building.html).
