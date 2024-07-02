# Use Debian Bullseye as the base image
FROM mcr.microsoft.com/devcontainers/base:bullseye

# Update the package list and install necessary packages
RUN apt-get update && apt-get install -y \
    texlive-latex-base \
    texlive-latex-extra \
    texlive-extra-utils \
    texlive-fonts-extra \
    texlive-lang-german \
    biber \
    latexmk \
    git \
    vim

# Set the working directory
WORKDIR /workspace

# Copy the project files to the container
COPY . .

# Setup .bashrc
RUN echo 'alias ll="ls -lah --color=auto"' >> ~/.bashrc

# Set the default command to run when the container starts
CMD ["sleep", "infinity"]
