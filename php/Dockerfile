FROM ubuntu:latest

WORKDIR /app

RUN apt update -y && apt upgrade -y
RUN apt install -y curl
RUN apt install -y zip
RUN apt install -y nodejs
RUN apt install -y npm

# Set TERM to avoid errors
ENV TERM=xterm

# Install PHP non-interactively
RUN DEBIAN_FRONTEND=noninteractive /bin/bash -c "$(curl -fsSL https://php.new/install/linux/8.4)"

# Ensure environment variables are loaded
RUN echo "source /root/.bashrc" >> /root/.bashrc

EXPOSE 8080

CMD [ "bash" ]
