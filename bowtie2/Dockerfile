#DOCKERFILE for bowtie2
FROM ubuntu:16.04
MAINTAINER Rafael Mamede, rmamede@medicina.ulisboa.pt

#INSTALL DEPENDENCIES
RUN apt-get update
RUN apt-get -y install unzip wget gcc g++ libtbb-dev

WORKDIR /NGStools/
ENV work_dir="/NGStools/bowtie2-2.3.2"

RUN wget https://downloads.sourceforge.net/project/bowtie-bio/bowtie2/2.3.2/bowtie2-2.3.2-linux-x86_64.zip
RUN unzip bowtie2-2.3.2-linux-x86_64.zip
RUN rm -rf bowtie2-2.3.2-linux-x86_64.zip

#ADD BOWTIE TO PATH
ENV PATH="${work_dir}:${PATH}"

RUN bowtie2 --help

