# docker/drivechain/Dockerfile

FROM ubuntu:20.04

# Install necessary dependencies
RUN apt-get update && \
    apt-get install -y wget unzip

# Download and unzip the drivechain binary
RUN wget https://releases.drivechain.info/L1-Mainchain-latest-x86_64-unknown-linux-gnu.zip && \
    unzip L1-Mainchain-latest-x86_64-unknown-linux-gnu.zip -d /drivechain && \
    chmod +x /drivechain/L1-Mainchain-latest-x86_64-unknown-linux-gnu/drivechain-qt

# Expose necessary ports
EXPOSE 8332 8333

# Start the drivechain node
CMD ["/drivechain/L1-Mainchain-latest-x86_64-unknown-linux-gnu/drivechain-qt", "-daemon"]