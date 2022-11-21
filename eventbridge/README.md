# eventbridge
A _Python 3.10_ service that streams events on an event queue and from there writes it into the datalake.
This service is build with poetry.

## Prerequisites
* Ensure you have [GNU make](https://www.gnu.org/software/make/) installed (if you're a windows user read [this section](/jobs#note-for-windows-users) below)
* Python >= 3.10, you can use for example [pyenv](https://github.com/pyenv/pyenv#installation) to manage that
* [Poetry](https://python-poetry.org/docs/#installation)
* [librdkafka](https://github.com/confluentinc/confluent-kafka-python#prerequisites)

### Note for Windows users

Ensure `make` is available, if not, please install it by of the below mentioned routes:

* Powershell: Install `make` via [chocolatey](https://chocolatey.org/install): `choco install make`
* WSL 2: Setup the [Windows Subsystem for Linux 2](https://learn.microsoft.com/en-us/windows/wsl/about) and install `make`
* Docker: Install [Docker](https://docs.docker.com/desktop/install/windows-install/) and create a Docker container with `make` installed

## Installing dependencies
```bash
make install
```

### Ensure setup is working and ready for the challenge
```bash
make check-setup
```

## Tests and checks
To run all tests and checks:
```bash
make check
```

To run all tests (unit and integration):
```bash
make test
```

### unit-tests
To just run unit-tests:
```bash
make unit-test
```

### integration-tests
To just run integration-tests:
```bash
make integration-test
```

### Auto-formatting
```bash
make auto-format
```

### Linting
```bash
make lint
```

### Check types
```bash
make type-check
```

## Data flow
![eventbridge-architecture](../docs/eventbridge-architecture.png)
