# DH2CI
Saving Docker Hub images in codeinside.ru registry

Variable:

DOCKER_HUB_IMAGE = postgres

Use template
```
---
include:
  - project: 'tools/continuous-integration/docker/dh2ci'
    file: 'gitlab-ci.yml'
    ref: master

##########################################################################################################

variables:
  DOCKER_HUB_TAG:
    value: "latest"
    description: "ОБЯЗАТЕЛЬНАЯ ПЕРЕМЕННАЯ!!!: указываем необходимый тэг"
  GIT_DEPTH: 1
  TRUNK_TAG: $DOCKER_HUB_TAG

##########################################################################################################

## PIPELINE DEFINITION
stages:
  - pack

```
