# raspberry toolbox
This is a toolbox for various testing and troubleshooting for raspberry.

# Run in kubernetes
kubectl run -ti toolbox --image=ludwigprager/toolbox-arm32v6 -- /bin/bash

# Run in docker
docker run -ti \
  --name toolbox \
  ludwigprager/toolbox-arm32v6 \
  /bin/bash

or

docker exec -ti toolbox /bin/sh

# Build

source set-env.sh
docker build -t $TOOLBOX_ARM32_IMAGE .
