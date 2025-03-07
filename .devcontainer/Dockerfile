# Build the Go Binary
FROM registry.suse.com/bci/golang:1.23 as build

RUN apt-get update
#RUN apt-get install vim sudo curl -y
RUN apt-get install vim sudo curl git jq -y

RUN useradd -m -s /bin/bash -G sudo coder
USER coder

# Let's add a fancy prompt!
RUN echo "PS1='🐳 \[\033[1;36m\]\h \[\033[1;34m\]\W\[\033[0;35m\] \[\033[1;36m\]# \[\033[0m\]'"  >> /home/coder/.bashrc
