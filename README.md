## Minimal Maven Docker Image

### Usage
    docker run --rm -it \
           -v $PWD:/src \
           aibar/mvn \
           mvn clean package

### If you have something special in ".m2"
    docker run --rm -it \
           -v $PWD:/src \
           -v $HOME/.m2:/.m2 \
           aibar/mvn \
           mvn clean package