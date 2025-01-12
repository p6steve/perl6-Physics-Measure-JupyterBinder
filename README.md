[![License: Artistic-2.0](https://img.shields.io/badge/License-Artistic%202.0-0298c3.svg)](https://opensource.org/licenses/Artistic-2.0)
[![rpmjk -> DH](https://github.com/librasteve/raku-Physics-Measure-Jupyter/actions/workflows/rpmjk-weekly.yaml/badge.svg)](https://github.com/librasteve/raku-Physics-Measure-Jupyter/actions/workflows/rpmjk-weekly.yaml)

## raku-Physics-Measure-Jupyter
Jupyter workbook examples for raku [Physics::Measure](https://github.com/librasteve/raku-Physics-Measure)

A set of SI, Imperial and US Unit classes that are employed as Measure objects having value, units and error that can act as operands in most calculations. Some prefix and physical constants included where needed.

## Docker Instructions
To use on Docker:
- ```docker run -it -p 8888:8888 librasteve/rakudo:rpmjk```
- ```jupyter-notebook --port=8888 --no-browser --allow-root```

_running on root is NOT RECOMMENDED, this is NOT SUITABLE for public facing servers_

_copy config to ~/.jupyter/jupyter_notebook_config.json to disable password (also very insecure)_

_go jupyter notebook --generate-config, then c.NotebookApp.quit_button = False to disable Quit button_

_detach gracefully with Ctrl-P, Ctrl-Q if you want the server to outlive your terminal_

_on Apple M-series silicon, Docker Desktop will run it on rosetta ([settings](https://levelup.gitconnected.com/docker-on-apple-silicon-mac-how-to-run-x86-containers-with-rosetta-2-4a679913a0d5))_

## Installation Instructions
To install on your local machine:
- ```zef install --verbose https://github.com/librasteve/raku-Physics-Measure.git```
- do the Quick Start here Brian Duggan perl6 jupyter-notebook at <https://github.com/bduggan/p6-jupyter-kernel>
- ```git clone https://github.com/librasteve/raku-Physics-Measure-Jupyter.git``` this repo on your machine and ```cd raku-Physics-Measure-Jupyter``` into the new dir
- command line ```jupyter-notebook``` - this will open a jupyter-notebook session in your browser
- in the browser, go to /eg and click Synopsis.ipynb, then Run each cell - explore & enjoy!

## Build Instructions
To build the Docker image from scratch (multiarchitecture):

```docker buildx build --platform linux/amd64,linux/arm64 -t librasteve/rakudo:rpmjk .```

NB. Enable the containerd image store in the Docker Desktop settings for buildx support.

## Inspired by
* Brian Duggan's perl6 jupyter-notebook at <https://github.com/bduggan/p6-jupyter-kernel>

Copyright (c) Henley Cloud Consulting Ltd. 2024
