# CADFACTS 

## How to run

### Before Running ensure shared_network is created

```sh
docker network inspect shared_network

#if not
docker network create shared_network
```


### Running Backend

```sh
docker compose -f test.compose.yml up
```

### Running Orthanc (OHIF Repository)

```sh
yarn run orthanc:up
```

### Running OHIF Viewer (OHIF Repository)

```sh
# If you haven't already, enable yarn workspaces
yarn config set workspaces-experimental true

# Restore dependencies
yarn install

# Run our dev command, but with the local orthanc config
yarn run dev:orthanc
```

### Running Frotend

```sh
yarn

yarn dev
```
