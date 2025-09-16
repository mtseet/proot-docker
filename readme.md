
# proot-docker
Run docker containers using proot

## Description
Provides all the necessary options to run containers using proot
```
proot-docker - Docker containers using proot
Available commands
  run
  pull
  ps
  rm
  images
  help
```

## Dependencies
proot, skopeo, jq

## Installation 

```
sudo apt update
sudo apt install proot skopeo jq
```

## Example usage
- pull image
```
./proot-docker pull ubuntu:jammy
```

- run container

```
./proot-docker run ubuntu:jammy -b /tmp:/tmp /bin/bash
```

- see available containers

```
./proot-docker ps
```

- see available images

```
./proot-docker images
```

- remove container

```
./proot-docker rm ubuntu:jammy
```

- remove image

```
./proot-docker rmi ubuntu:jammy
```

## Special notes
Works on termux but you will have to run skopeo using proot. You have to some how download and extract the skopeo docker image. There is no skopeo binary available for termux
