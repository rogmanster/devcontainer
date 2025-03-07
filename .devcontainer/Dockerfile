FROM registry.suse.com/bci/golang:1.23 as build

# Refresh and install required packages
RUN zypper refresh && zypper install -y vim sudo curl shadow

# Create the 'coder' user with sudo access (SUSE-specific)
RUN useradd -m -s /bin/bash -G users coder && echo "coder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/coder

# Ensure the .bashrc file is modified for the 'coder' user
RUN echo 'export PS1="🐳 \[\033[1;36m\]\h \[\033[1;34m\]\W\[\033[0;35m\] \[\033[1;36m\]# \[\033[0m\]"' >> /home/coder/.bashrc

# Switch to 'coder' user
USER coder

