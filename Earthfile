VERSION 0.8
FROM debian:12-slim
WORKDIR /app
build:
  RUN apt-get update && \
      apt-get install -y build-essential zlib1g-dev && \
      apt-get clean && \
      rm -rf /var/lib/apt/lists/*
  COPY src/* /app/
  RUN make
  SAVE ARTIFACT nii2mesh AS LOCAL nii2mesh