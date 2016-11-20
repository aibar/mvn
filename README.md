## Minimal Maven Docker Image

    FROM walkingdevs/mvn

### Usage
    docker run --rm -it \
           -v $PWD:/src \
           -w /src
           walkingdevs/mvn \
           mvn package

### If you have something special in ".m2"
    docker run --rm -it \
           -v $PWD:/src \
           -v $HOME/.m2:/m2 \
           -w /src
           walkingdevs/mvn \
           mvn package