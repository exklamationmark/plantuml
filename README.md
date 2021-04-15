PlantUML tools
==============

This repo package tools for making diagrams with [PlantUML](https://plantuml.com/).

We aim to release these thing(s):

- Images, e.g: `exklamationmark/plantuml:latest` that package PlantUML into
  a container => run anywhere.
- A helm chart for running [PlantUML-server](https://github.com/plantuml/plantuml-server)
  on Kubernetes, so you don't need to paste sensitive diagrams on the Internet.

Tags follow [PlantUML's releases](https://github.com/plantuml/plantuml/releases).

Usage
-----

```bash
# generate SVG image
docker run --rm -i exklamationmark/plantuml:latest < example.uml \
	> diagram.svg

# generate PNG image
cat example.uml | docker run --rm -i exklamationmark/plantuml:latest -tpng \
	> diagram.png
```

Develop
-------

You will need these installed:

- [Docker](https://docs.docker.com/engine/install/)
- [GNU Make](https://www.gnu.org/software/make/)
- [Git](https://git-scm.com/)
- [git-flow](https://github.com/nvie/gitflow/wiki/Manual-installation)
- [git LFS](https://git-lfs.github.com/)


How things are done:

- Use `git-flow` to develop, branch and release.
- We track large binary files with `git lfs` (so there is a local copy + don't
  depend on Internet access).