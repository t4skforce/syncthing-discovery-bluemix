# syncthing-discovery-bluemix
This Docker Container was crafted for easy Bluemix deployment, it is based on [https://hub.docker.com/r/t4skforce/syncthing-discovery/](syncthing-discovery) and is configurable the same way.

The files for this container can be found at my [GitHub repo](https://github.com/t4skforce/syncthing-discovery-bluemix)

[![](https://images.microbadger.com/badges/image/t4skforce/syncthing-discovery-bluemix.svg)](http://microbadger.com/images/t4skforce/syncthing-discovery-bluemix "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/t4skforce/syncthing-discovery-bluemix.svg)](http://microbadger.com/images/t4skforce/syncthing-discovery-bluemix "Get your own version badge on microbadger.com")

# How to use this image

## Pull Image Locally
`docker pull t4skforce/syncthing-discovery-bluemix:latest`

## Push Image Remotely
`docker tag t4skforce/syncthing-discovery-bluemix:latest registry.ng.bluemix.net/<repository>/syncthing-discovery-bluemix:latest`

`docker push registry.ng.bluemix.net/<repository>/syncthing-discovery-bluemix:latest`


## Setup Bluemix Container
1. Open Bluemix dashboard
2. Open Containers
3. Create Container
4. Select "syncthing-discovery-bluemix"
5. Setup Public IP
6. Setup Volume to path: `/home/discosrv/certs`

## Upload local certificates to volume
`bluemix ic cp ./cert.pem <containerid>:/home/discosrv/certs`

`bluemix ic cp ./key.pem <containerid>:/home/discosrv/certs`