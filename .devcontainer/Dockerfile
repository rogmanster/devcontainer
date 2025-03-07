# Build the Go Binary
FROM registry.suse.com/bci/golang:1.23 as build

RUN zypper refresh && zypper install -y vim sudo curl

# Create user 'coder' with home directory and shell access
RUN adduser -m -s /bin/bash coder && usermod -aG sudo coder

RUN echo "coder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/coder

# Ensure the .bashrc file is modified correctly
RUN echo 'export PS1="🐳 \[\033[1;36m\]\h \[\033[1;34m\]\W\[\033[0;35m\] \[\033[1;36m\]# \[\033[0m\]"' >> /home/coder/.bashrc

# Ensure permissions are correct
RUN chmod 644 /home/coder/.bashrc

# Set working directory to home
WORKDIR /home/coder

CMD ["bash"]
