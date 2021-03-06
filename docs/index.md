<h1 align="center">
  Watchtower
</h1>

<p align="center">
  A container-based solution for automating Docker container base image updates.
  <br/><br/>
  <a href="https://circleci.com/gh/containrrr/watchtower">
    <img alt="Circle CI" src="https://circleci.com/gh/containrrr/watchtower.svg?style=shield" />
  </a>
  <a href="https://godoc.org/github.com/containrrr/watchtower">
    <img alt="GoDoc" src="https://godoc.org/github.com/containrrr/watchtower?status.svg" />
  </a>
  <a href="https://microbadger.com/images/containrrr/watchtower">
    <img alt="Microbadger" src="https://images.microbadger.com/badges/image/containrrr/watchtower.svg" />
  </a>
  <a href="https://goreportcard.com/report/github.com/containrrr/watchtower">
    <img alt="Go Report Card" src="https://goreportcard.com/badge/github.com/containrrr/watchtower" />
  </a>
  <a href="https://github.com/containrrr/watchtower/releases">
    <img alt="latest version" src="https://img.shields.io/github/tag/containrrr/watchtower.svg" />
  </a>
  <a href="https://www.apache.org/licenses/LICENSE-2.0">
    <img alt="Apache-2.0 License" src="https://img.shields.io/github/license/containrrr/watchtower.svg" />
  </a>
  <a href="https://www.codacy.com/app/simskij/watchtower">
    <img alt="Codacy Badge" src="https://api.codacy.com/project/badge/Grade/3a4d0fcfd26d45b09b1d7ea3c8c13744"/>
  </a>
  <a href="https://www.codacy.com/app/simskij/watchtower?utm_source=github.com&utm_medium=referral&utm_content=containrrr/watchtower&utm_campaign=Badge_Coverage">
    <img alt="Codacy Badge" src="https://api.codacy.com/project/badge/Coverage/3a4d0fcfd26d45b09b1d7ea3c8c13744" />
  </a>
  <a href="https://gitter.im/containrrr/watchtower?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge">
    <img alt="Join the chat at https://gitter.im/containrrr/watchtower" src="https://badges.gitter.im/containrrr/watchtower.svg" />
  </a>
  <a href="#contributors">
    <img alt="All Contributors" src="https://img.shields.io/badge/all_contributors-30-orange.svg?style=flat-square" />
  </a>
</p>

## Quick Start

With watchtower you can update the running version of your containerized app simply by pushing a new image to the Docker Hub or your own image registry. Watchtower will pull down your new image, gracefully shut down your existing container and restart it with the same options that were used when it was deployed initially. Run the watchtower container with the following command:

```
$ docker run -d \
    --name watchtower \
    -v /var/run/docker.sock:/var/run/docker.sock \
    containrrr/watchtower
```