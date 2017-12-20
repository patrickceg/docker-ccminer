# docker-ccminer

## How to use

Prerequisite: A machine (physical or virtual) that can use CUDA-enabled GPUs; How new of a GPU, or the CUDA compute capability of the card, depends on the algorithm you are mining

### Installing stuff to make this run

1. Install the Cuda drivers for your machine (this depends on the Linux distribution, but you can also consult the nVidia downloads page to see which distributions are supported https://developer.nvidia.com/cuda-downloads?target_os=Linux )
2. Install nvidia-docker https://github.com/NVIDIA/nvidia-docker

### Usage example

assuming you are running as root or as a user that is part of the _docker_ group):

`nvidia-docker run --rm patrickceg/ccminer:cuda9 ccminer -a lyra2v2 -o stratum+tcp://imaginedpool.doesnotexist.net:1234 -u myuser.w1 -p x`

This example mines with the settings:

* Algorithm lyra2v2
* Server using stratum+tcp on imaginedpool.doesnotexist.net port 1234
* Username myuser.w1
* Password x

## About the Docker image / Github

This is an experiment with ccminer from https://github.com/tpruvot/ccminer

I have used this personally to mine for a few months now on a GTX 1080

The Docker Hub build https://hub.docker.com/r/patrickceg/ccminer/

The repository https://github.com/patrickceg/docker-ccminer
