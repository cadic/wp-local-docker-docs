## Prerequisites

WP Local Docker requires docker, docker-compose, Node 8, and npm. It is recommended that you use the latest versions of 
docker and docker-compose. Node 8 (current LTS version) is the only version of node that is supported. While WP Local 
Docker _may_ work with other versions of Node, compatibility is not guaranteed.

#### MacOS
Docker is available for download from the [Docker website](https://docs.docker.com/docker-for-mac/install/) and will
install docker-compose automatically. NodeJS and npm can be installed from the [NodeJS website](https://nodejs.org),
via a package manager, such as [Homebrew](https://brew.sh/), or using a version manager, such as 
[nvm](https://github.com/creationix/nvm).  

##### NodeJS EACCESS Error
If Node was installed via the download from the NodeJS website, you will likely get an `EACCESS` error when trying to install
global npm packages without using sudo. Npm has an article on [preventing permission errors](https://docs.npmjs.com/getting-started/fixing-npm-permissions#option-2-change-npms-default-directory-to-another-directory)
if you'd like to run the command without sudo. Alternatively, just run the install command with sudo.

#### Windows
Docker is available for download from the [Docker website](https://docs.docker.com/docker-for-windows/install/) and will
install docker-compose automatically. NodeJS and npm can be installed from the [NodeJS website](https://nodejs.org).

#### Linux
Docker has platform specific installation instructions available for linux on their [documentation site](https://docs.docker.com/install/#supported-platforms).
Once docker is installed, you will need to [manually install docker compose](https://docs.docker.com/compose/install/).
NodeJS can be installed via a package manager for many linux platforms [following these instructions](https://nodejs.org/en/download/package-manager/).

## Installation

Once all installation prerequisites have been met, WP Local Docker is installed as a global npm package by running
`npm install -g wp-local-docker-generator`. You can confirm it has been installed by running `10updocker --version`.

## Configuration

The first time you run a WP Local Docker command, you will be asked if you want to use configuration defaults.
By default, WP Local Docker will store all environments within `~/wp-local-docker-sites`. If you would like to customize
this path, run `10updocker configure` and enter your desired path.

## Updating

To update WP Local Docker, run `npm update -g wp-local-docker-generator`