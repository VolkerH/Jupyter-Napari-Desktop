# Setting up a remote desktop to use Napari in a browser

* Do you want to run a course/workshop on napari or other GUI based-tools and worry how all participants can have a working python environment?
* Do you want to deploy some software that needs a GUI on a powerful-GPU workstation with good connection to the storage where users have large datasets?

Setting up a remote desktop environment that can be accessed via a web browser might be a possible solution to these problems.
This repo contains some basic documentation on how to set up such a remote desktop environment with Docker containers. It is based on 
[jupyter-desktop-server by yuvipanda](https://github.com/yuvipanda/jupyter-desktop-server). A similar approach has been used with binder in NEUBIAS training for napari based on an idea by [guiwitz](https://github.com/guiwitz/).

# tl;dr 

TODO: pull a docker image from the hub and run it
Show animated gif

# Simple Recipe to build a jupyter desktop image with napari

## Docker and containers

If you never heard about Docker and containers, it is probably a good idea to read or watch a short introductory tutorial.
As a minimum requirement you need to install docker on your system. The basic instructions should work on Linux, Windows and Mac but the author has only tested them on Linux. In particular, shell scripts might differ a bit on windows depending on whether you use `cmd.exe`, Powershell or `bash` from WSL2. 
If you plan on providing CUDA-based GPU acceleration for machine learning libraries (`tensorflow`, `pytorch`) or array libraries (`cupy`) make sure you install the NVIDIA-Docker runtime (NVIDIA docker is limited to Linux and not supported on Mac. It may work on windows using WSL2).

## Base image

As a first step, we just build a docker image to run a bare-bones jupyter desktop. All the necessary files are in [`01-jupyter-desktop`](./01-jupyter-desktop). This have basically just been vendored (fancy name for copied into this repo) from the official [Jupyter project](https://github.com/jupyterhub/jupyter-remote-desktop-proxy).


## Modifying the base image or building on top?

## Add a python environment with napari

## Customizations


# Add GPU support

# Build images in CI

# Mount Volumes


# Deploy on a server for multiple users

## Jupyterhub


## Custom solution