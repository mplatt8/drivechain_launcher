# docker/sidechain/Dockerfile

FROM ubuntu:20.04

# Install necessary dependencies
RUN apt-get update && \
    apt-get install -y build-essential git

# Clone the repository and build the sidechain
RUN git clone https://github.com/mplatt8/drivechain_launcher.git /drivechain_launcher && \
    cd /drivechain_launcher && \
    make

# Expose necessary ports
EXPOSE 12345 12346

# Start the sidechain node
CMD ["/drivechain_launcher/start_sidechain.sh"]