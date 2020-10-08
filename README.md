# Raspberrypi Toolbox
This is a toolbox for various testing and troubleshooting for raspberry.

# Run In Kubernetes
kubectl run -ti --rm toolbox-$RANDOM --image=ludwigprager/toolbox-arm32v6:1

# Run In Docker
docker run -ti \
  --name toolbox \
  ludwigprager/toolbox-arm32v6 \
  /bin/bash

or

docker exec -ti toolbox /bin/sh

# Build The Image On A Raspberry Yourself
source set-env.sh
docker build -t $TOOLBOX_ARM32_IMAGE .
