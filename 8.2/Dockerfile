FROM ubuntu:18.04
MAINTAINER TT <edy555@gmail.com>
LABEL Description="Docker image for building arm-embedded projects"

# Install any needed packages specified in requirements.txt
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y make git bzip2 wget && \
    apt-get clean && \
    wget https://developer.arm.com/-/media/Files/downloads/gnu-rm/8-2018q4/gcc-arm-none-eabi-8-2018-q4-major-linux.tar.bz2 -O - | tar xj

ENV PATH "/gcc-arm-none-eabi-8-2018-q4-major/bin:$PATH"
WORKDIR /work
