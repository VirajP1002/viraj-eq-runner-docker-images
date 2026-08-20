# Google Cloud Datastore Emulator Image

This image provides a dockerised version of the [Google Cloud Datastore Emulator](https://cloud.google.com/datastore/docs/tools/datastore-emulator). It is intended to be used as a service for development and test. It is **NOT** intended be used in formal environments.

[Google Datastore](https://cloud.google.com/datastore/) is a flexible, scalable No SQL database service.

### Useful commands

Build a new image locally by running:
```sh
docker build . -t gcloud-datastore-emulator:local
```
Run a container by running:
```bash
docker run --name gcloud-datastore-emulator -p 8432:8432 -p 8989:8989 -e CLOUDSDK_CORE_PROJECT=local gcloud-datastore-emulator:local
```
Exec into the container by running:
```bash
docker exec -i -t -u root gcloud-datastore-emulator /bin/sh
```
Once in the container check the gcloud components
```bash
gcloud components list --show-versions
```
