# SW Checkin

[![Build Status](https://travis-ci.org/pyro2927/SouthwestCheckin.svg?branch=master)](https://travis-ci.org/pyro2927/SouthwestCheckin)
[![Maintainability](https://api.codeclimate.com/v1/badges/aa1c955dfcba58a7352f/maintainability)](https://codeclimate.com/github/pyro2927/SouthwestCheckin/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/aa1c955dfcba58a7352f/test_coverage)](https://codeclimate.com/github/pyro2927/SouthwestCheckin/test_coverage)
[![Docker Build Status](https://img.shields.io/docker/automated/pyro2927/southwestcheckin.svg?style=flat)](https://hub.docker.com/r/pyro2927/southwestcheckin)
[![Docker Image Size](https://images.microbadger.com/badges/image/pyro2927/southwestcheckin.svg)](https://microbadger.com/images/pyro2927/southwestcheckin)

![](http://www.southwest-heart.com/img/heart/heart_1.jpg)

This python script checks your flight reservation with Southwest and then checks you in at exactly 24 hours before your flight.  Queue up the script and it will `sleep` until the earliest possible check-in time.

## Contributors

[![](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/images/0)](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/links/0)[![](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/images/1)](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/links/1)[![](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/images/2)](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/links/2)[![](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/images/3)](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/links/3)[![](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/images/4)](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/links/4)[![](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/images/5)](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/links/5)[![](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/images/6)](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/links/6)[![](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/images/7)](https://sourcerer.io/fame/pyro2927/pyro2927/SouthwestCheckin/links/7)


## Requirements

This script can either be ran directly on your host or within Docker.

### Host

* Python (should work with 2.x or 3.x thanks to @ratabora)
* [pip](https://pypi.python.org/pypi/pip)

### Docker

* Docker (tested with 1.12.6)

## Setup

### Host

#### Install Base Package Requirements

```bash
$ pip install -r requirements.txt
```

#### Usage

```bash
$ python ./checkin.py CONFIRMATION_NUMBER FIRST_NAME LAST_NAME
```

### Docker

#### Usage

```bash
$ sudo docker run -it frankhsu/southwestcheckin:latest CONFIRMATION_NUMBER FIRST_NAME LAST_NAME
```

#### update headers.txt
from the network console found in the request to /review
when attempting to check in
i.e. https://www.southwest.com/air/check-in/review.html?hash=c1faf1f2-7233-403d-a9de-620d54be0820&searchToken=M2dNFOzwvino9s7HerGCzUVT3l3U1f-wqqeE2gidh3LghCHghMXEB6aj5B6R6lnFrg9sXPaiF40ZfBv-2hYOON8hgk4HwhhKEBHyFWQaRTslSmbDXJZ2zsHkP4dsS05-154fTLfjTwPVUAg%3D
