FROM ubuntu:18.04
MAINTAINER TT <edy555@gmail.com>
LABEL Description="Docker image for building arm-embedded projects"

# Install any needed packages specified in requirements.txt
RUN apt update && \
    apt upgrade -y && \
    apt install -y make git zip bzip2 wget lib32z1 lib32ncurses5 && \
    apt clean && \
    wget https://launchpad.net/gcc-arm-embedded/4.9/4.9-2015-q3-update/+download/gcc-arm-none-eabi-4_9-2015q3-20150921-linux.tar.bz2 -O tmp.tar.bz2 && \
    tar -xjf tmp.tar.bz2 && \
    rm tmp.tar.bz2

ENV PATH "/gcc-arm-none-eabi-4_9-2015q3/bin:$PATH"
WORKDIR /work
