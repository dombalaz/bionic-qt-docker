# Docker bionic-qt

This image provides Qt libraries running on Ubuntu Bionic inside docker.

## Getting Started

These instructions will help you to run this docker image on your machine.

### Prerequisites

In order to run the image you have to install [Docker](https://www.docker.com/get-started).

### Run

#### Docker Hub

If you have docker installed you can pull and run image from [Docker Hub](https://hub.docker.com/repository/docker/mink0/bionic-qt) as

```sh
docker run -it mink0/bionic-qt
```

Image provides multiple versions of Qt, see [available tags](https://hub.docker.com/repository/docker/mink0/bionic-qt/tags) for more informations.

#### Local Build

You can also clone this repo and build the image yourself. The image uses Qt online installer with gui script. In order to installer to work, you have to provide build arguments `QT_CI_LOGIN` and `QT_CI_PASSWORD`. These should be your login credentials to Qt account. You can also specify argument `QT_VERSION` to build specific version (keep in mind that only latest and supported versions are supported by installer script).

```sh
git clone https://github.com/dombalaz/bionic-qt-docker && cd bionic-qt-docker
docker build --build-arg QT_CI_LOGIN="login" --build-arg QT_CI_PASSWORD="password" --build-arg QT_VERSION="5.15.0" .
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for more details.
