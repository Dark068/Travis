FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

# Set working directory
WORKDIR /workspace

# Copy all repository files into container
COPY . /workspace

# Install system dependencies
RUN apt-get update && apt-get install -y \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

# Upgrade pip and install Python dependencies
RUN pip3 install --no-cache-dir --upgrade pip && \
    pip3 install --no-cache-dir -r requirements.txt

# Make the binary executable
RUN chmod +x suhani
