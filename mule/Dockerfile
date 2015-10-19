#
# Mule ESB 3.7.0  Dockerfile
#
#

# Pull base image(ubuntu latest)
FROM base

# Author
MAINTAINER karpra

# Download Mule ESB 3.7.0 & Install it.
RUN \
    apt-get update && DEBIAN_FRONTEND=noninteractive apt-get -y install libpcre3 libssl-dev libpcre3-dev wget zip gcc default-jdk && \
    cd /opt && wget --no-check-certificate  https://repository-master.mulesoft.org/nexus/content/repositories/releases/org/mule/distributions/mule-standalone/3.7.0/mule-standalone-3.7.0.tar.gz && \
    tar xvzf mule-standalone-3.7.0.tar.gz && \
    rm mule-standalone-3.7.0.tar.gz && \
    ln -s /opt/mule-standalone-3.7.0 /opt/mule 



# Define default command.
CMD ["/bin/sh","-c","/opt/mule/bin/mule"]

# Expose ports.
EXPOSE 8888
