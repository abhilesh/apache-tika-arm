# apache-tika-arm
Docker images to run Apache Tika server on `armhf` and `arm64` systems. In theory these images are identical to those of [apache/tika-docker](https://github.com/apache/tika-docker).

Find the images at https://hub.docker.com/r/abhilesh7/apache-tika-arm/

----
## Documentation from official Apache Tika Server Repository

This repo is used to create convenience Docker images for Apache Tika Server published as [apache/tika](https://hub.docker.com/r/apache/tika) on DockerHub by the [Apache Tika](http://tika.apache.org/) Dev team

The images create a functional Apache Tika Server instance that contains the latest Ubuntu running the appropriate version's server on Port 9998 using Java 8 (until version 1.20), Java 11 (1.21 and 1.24.1), Java 14 (until 1.27/2.0.0), and Java 16 for newer versions.

There is a minimal version, which contains only Apache Tika and it's core dependencies, and a full version, which also includes dependencies for the GDAL and Tesseract OCR parsers. To balance showing functionality versus the size of the full image, this file currently installs the language packs for the following languages:

English
French
German
Italian
Spanish.
To install more languages simply update the apt-get command to include the package containing the language you required, or include your own custom packs using an ADD command.

----

## Usage

Pull the image using:

```docker pull docker pull abhilesh7/apache-tika-arm:latest```

Run the container using:

```docker run -d -p 9998:9998 abhilesh7/apache-tika-arm:latest```

----
I originally created this image for use with [Paperless-ng](https://github.com/jonaswinkler/paperless-ng) on a Raspberry Pi 4.

A template docker-compose file for installing paperless-ng on `arm` systems can be found at - https://github.com/abhilesh/self-hosted_docker_setups/tree/main/paperless-ng
