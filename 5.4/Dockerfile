FROM ubuntu:18.04
MAINTAINER TT <edy555@gmail.com>
LABEL Description="Docker image for building arm-embedded projects"

# Install any needed packages specified in requirements.txt
RUN apt update && \
    apt upgrade -y && \
    apt install -y make git bzip2 wget lib32z1 lib32ncurses5 && \
    apt clean && \
    wget https://developer.arm.com/-/media/Files/downloads/gnu-rm/5_4-2016q3/gcc-arm-none-eabi-5_4-2016q3-20160926-linux.tar.bz2 -O tmp.tar.bz2 && \
    tar -xjf tmp.tar.bz2 && \
    rm tmp.tar.bz2

ENV PATH "/gcc-arm-none-eabi-5_4-2016q3/bin:$PATH"
WORKDIR /work
