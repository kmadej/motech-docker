FROM ubuntu:12.04

RUN apt-get update

# Set up repo
RUN apt-get install --yes python-software-properties
RUN add-apt-repository --yes ppa:webupd8team/java
RUN apt-get update

# Set some vars so the oracle installer doesn't ask us to accept the license
RUN echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections
RUN echo debconf shared/accepted-oracle-license-v1-1 seen true | debconf-set-selections

# Install JDK 7
RUN apt-get install --yes oracle-java7-installer

# Install JDK 8
RUN apt-get install --yes oracle-java8-installer
