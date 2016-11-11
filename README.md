## Minimal Maven Docker Image

    FROM walkingdevs/mvn:3.3.9

### Usage
    docker run --rm -it \
           -v $PWD:/src \
           walkingdevs/mvn \
           clean package

### If you have something special in ".m2"
    docker run --rm -it \
           -v $PWD:/src \
           -v $HOME/.m2:/m2 \
           walkingdevs/mvn \
           clean package