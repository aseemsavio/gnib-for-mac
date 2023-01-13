# gnib-for-mac

Since Graal VM Native Images cannot be cross compiled for other operating systems, it often becomes a bit of a hassle
to build these images from M1 Macs.

This project lets one build ARM based Native images for Linux from Macs.

#### Building the image locally
```
docker build --no-cache -t aseemsavio/builder .
```

#### Running the container
```
docker container run -ti aseemsavio/builder
```

#### Getting contents of a folder inside the container.

This command copies the contents of `/src` folder in the host to `/target` folder in the container

```
docker cp src/. container_id:/target
```

#### Copy a file from container to host

```
docker cp container_id:/src/. target
```


