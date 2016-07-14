# gradle-caches

A docker image intended to be used with [docker-android-sdk](https://github.com/georgepapas/docker-android-sdk).

When used in conjunction with docker-android-sdk, ensures that gradle and all build dependencies are not downloaded for each build.


#Usage

create a docker volume based on this image

``docker create --name gradle-caches georgepapas/gradle-caches:latest``

Mount this volume when using your docker android image

``docker run --rm --volumes-from gradle-caches -v $(pwd):/opt/app android-sdk:latest clean testDebug``