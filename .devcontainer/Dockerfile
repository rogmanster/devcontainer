# Build the Go Binary
FROM registry.suse.com/bci/golang:1.23 as build

RUN apt-get update
RUN apt-get install vim sudo curl -y

RUN useradd -m -s /bin/bash -G sudo coder

USER coder

# Ensure the .bashrc file is modified correctly
RUN echo "PS1='🐳 \[\033[1;36m\]\h \[\033[1;34m\]\W\[\033[0;35m\] \[\033[1;36m\]# \[\033[0m\]'" >> /home/coder/.bashrc

# Ensure permissions are correct
RUN chmod 644 /home/coder/.bashrc

# Set working directory to home
WORKDIR /home/coder

CMD ["bash"]
