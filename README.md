# github.com/jorgeLTS/docker-mysql
## About

This will build a Docker image for [MySQL](https://www.mysql.com/).

* Configuration tweaked to use all around settings for general usage - Can be changed
* Can use official Mysql environment variables (MYSQL_USER, MYSQL_PASSWORD, MYSQL_ROOT_PASSWORD)
* Allows for automatically creating multiple databases on container initialization

## Maintainer

- [Jorge Mendoza](https://github.com/jorgelts)

## Table of Contents

- [About](#about)
- [Maintainer](#maintainer)
- [Table of Contents](#table-of-contents)
- [Installation](#installation)
- [Configuration](#configuration)
  - [Quick Start](#quick-start)
  - [Persistent Storage](#persistent-storage)
  - [Customizable Settings](#customizable-settings)
  - [Environment Variables](#environment-variables)
    - [Base Images used](#base-images-used)
  - [Networking](#networking)
- [Maintenance](#maintenance)
  - [Shell Access](#shell-access)
- [Support](#support)
  - [Usage](#usage)
  - [Bugfixes](#bugfixes)
  - [Feature Requests](#feature-requests)
  - [Updates](#updates)
- [License](#license)
- [References](#references)

## Installation
* Download Docker Desktop for Mac or Windows. Docker Compose will be automatically installed. On Linux, make sure you have the latest version of Docker and Docker Compose.

* Clone this repository

```bash
docker-compose up -d
```

## Configuration

### Quick Start

* The quickest way to get started is using [docker-compose](https://docs.docker.com/compose/). See the example compose file.
* Set various [environment variables](#environment-variables) to understand the capabilities of this image.
* Map [persistent storage](#data-volumes) for access to configuration, data files and logs.
- Make [networking ports](#networking) available for public access if necessary

### Persistent Storage

The following directories are used for configuration and can be mapped for persistent storage.

| Directory           | Description                                                    |
| ------------------- | -------------------------------------------------------------- |
| `/var/lib/mysql`    | MySQL Data Directory                                           |
| `/etc/mysql/conf.d` | Optional directory to put .cnf files for additional directives |
| `/var/log/mysql`    | Logs directory                                                 |

### Customizable Settings
Optional directory to put .cnf files for additional directives

### Environment Variables

#### Base Images used

| Parameter                  | Description                                                  | Default          |
| -------------------------- | ------------------------------------------------------------ | ---------------- |
| `TZ`                       | Local time zone                                              | `America/Mexico_City` |

### Networking

The following ports are exposed.

| Port   | Description    |
| ------ | -------------- |
| `3306` | MySQL Server   |

## Maintenance

### Shell Access
For debugging and maintenance purposes you may want access the containers shell.

```bash
docker exec -it (whatever your container name is) bash
```

## Support

These images were built to serve a specific need in a production environment and gradually have had more functionality added based on requests from the community.

### Usage
- The [Discussions board](../../discussions) is a great place for working with the community on tips and tricks of using this image.
- Consider [sponsoring me](https://github.com/sponsors/tiredofit) personalized support.
### Bugfixes
- Please, submit a [Bug Report](issues/new) if something isn't working as expected. I'll do my best to issue a fix in short order.

### Feature Requests
- Feel free to submit a feature request, however there is no guarantee that it will be added, or at what timeline.
- Consider [sponsoring me](https://github.com/sponsors/tiredofit) regarding development of features.

### Updates
- Best effort to track upstream changes, More priority if I am actively using the image in a production environment.

## License
MIT. See [LICENSE](LICENSE) for more details.

## References

* https://www.mysql.com/