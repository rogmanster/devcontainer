FROM registry.suse.com/bci/golang:1.23 as build

# Refresh and install required packages
RUN zypper refresh && zypper install -y vim sudo curl shadow

# Modify the default user's Bash prompt
RUN echo 'export PS1="🐳 \[\033[1;36m\]\h \[\033[1;34m\]\W\[\033[0;35m\] \[\033[1;36m\]# \[\033[0m\]"' >> /root/.bashrc

# Set working directory
#WORKDIR /root

# Start the container with Bash
#CMD ["/bin/bash"]


