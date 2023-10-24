FROM mcr.microsoft.com/devcontainers/typescript-node:0-20
RUN apt-get update && apt-get install -y && apt-get clean

# Update to Yarn V3.6.3 from V1
RUN sudo corepack enable && yarn set version berry 

# Yarn V3.6.3
# Node V20.7.0
# TypeScript V5.1.3

# * Cloudflare Tunnel *

# Add cloudflare gpg key
RUN sudo mkdir -p --mode=0755 /usr/share/keyrings
RUN curl -fsSL https://pkg.cloudflare.com/cloudflare-main.gpg | sudo tee /usr/share/keyrings/cloudflare-main.gpg >/dev/null
# Add this repo to your apt repositories
RUN echo 'deb [signed-by=/usr/share/keyrings/cloudflare-main.gpg] https://pkg.cloudflare.com/cloudflared focal main' | sudo tee /etc/apt/sources.list.d/cloudflared.list
# install cloudflared
RUN sudo apt-get update && sudo apt-get install cloudflared -y && apt-get clean

# Add the following script to your package.json to configure Cloudflare Tunnel:
# "exposed-dev": "concurrently \"cloudflared tunnel --url http://host.docker.internal:3000\" \"npm run dev\"",