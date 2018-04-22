FROM ubuntu:16.04

RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:jonathonf/gcc
RUN apt-get update
RUN apt-get install -y gcc-7 g++-7
RUN update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 10
RUN update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-7 10

RUN apt-get install -y build-essential wget tar unzip uuid-dev make cmake git

RUN apt-get install -y subversion ninja alien m4 liblapack-dev libgsl0-dev libaio1 lib32z1 lib32stdc++6 \
        libyaml-dev libfftw3-dev jq bc libjansson-dev libtinyxml-dev libcurl4-openssl-dev libconfig++-dev \
        libmemcached11 libmemcached-dev liblog4cxx10-dev libpoco-dev libhiredis-dev libjsoncpp-dev libssl-dev \
        pkg-config zlib1g-dev libssl-dev libevent-dev python-dev python-setuptools libgmp-dev

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 379CE192D401AB61
RUN echo 'deb http://dl.bintray.com/lucidsoftware/apt/ main contrib' > /etc/apt/sources.list.d/lucidsoftware-contrib.list

RUN apt-get update
RUN apt-get install -y libaws-cpp-sdk-s3 # shared library
RUN apt-get install -y libaws-cpp-sdk-s3-dev # shared library
RUN apt-get install -y libaws-cpp-sdk-sqs # headers
RUN apt-get install -y libaws-cpp-sdk-sqs-dev # headers
RUN apt-get install -y libaws-cpp-sdk-sts # headers
RUN apt-get install -y libaws-cpp-sdk-sts-dev # headers
RUN apt-get install -y libaws-cpp-sdk-iam # headers
RUN apt-get install -y libaws-cpp-sdk-iam-dev # headers
RUN apt-get install -y libaws-cpp-sdk-core # headers
RUN apt-get install -y libaws-cpp-sdk-core-dev # headers


CMD ["bash", "loop.sh"]

