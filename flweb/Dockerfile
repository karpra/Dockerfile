#
# Flask & Pandas Dockerfile
#
# https://github.com/karpra/Dockerfile/flweb
#

# Pull base image.
FROM base

# Install Nginx.
RUN \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get install -y python python-dev python-pip python-pandas && \
  pip install Flask && \
  pip install --upgrade pandas && \
  rm -rf /var/lib/apt/lists/* && \
  mkdir -p /opt/services/app

# Define mountable directories.
VOLUME ["/opt/services/app"]

# Define working directory.
WORKDIR /opt/services/app

# Define default command.
CMD ["python app.py"]

# Expose ports.
EXPOSE 8000
