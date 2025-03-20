FROM sapmachine:21

# Install Node.js 22
RUN apt-get update
RUN apt-get install -y curl
RUN curl -fsSL https://deb.nodesource.com/setup_22.x | bash
RUN apt-get install -y nodejs

# Install git
RUN apt-get install -y git

# Install maven
RUN apt-get install maven -y

# Enable sudo support to configure deps reuse
ARG USERNAME=ubuntu
RUN apt-get install sudo -y \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME