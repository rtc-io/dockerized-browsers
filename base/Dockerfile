FROM ubuntu:14.04

# use aarnet mirror for quicker building while developing
RUN sed -i 's/archive.ubuntu.com/mirror.aarnet.edu.au\/pub\/ubuntu\/archive/g' /etc/apt/sources.list

# add scripts
ADD scripts/* /tmp/scripts/

# install baseline package dependencies
RUN apt-get -y update
RUN apt-get install -y curl wget software-properties-common build-essential git

# install xvfb
RUN apt-get install -y xvfb

# install loopback video
RUN /tmp/scripts/setup-loopbackvideo.sh
