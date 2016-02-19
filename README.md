# Building Ceylon DEB packages

The following images/tags are available:

 - `latest` ([ceylon-package-deb/Dockerfile](https://github.com/ceylon-docker/ceylon-package-deb/blob/master/Dockerfile))

To run the build perform the following steps:

 1. First make sure you have built the [Ceylon ZIP file](https://hub.docker.com/r/ceylon/ceylon-build/). The name of the ZIP file will be `ceylon-VERSION.zip` where `VERSION` is a number that will be used as an argument in step 3.
 2. `docker pull ceylon/ceylon-package-deb:latest`
 3. `docker run -t --rm -v /tmp/ceylon:/output ceylon/ceylon-package-deb:latest VERSION`

If the build completed successfully the resulting DEB file can be found in `/tmp/ceylon`.

NB: The `/tmp/ceylon` folder used in the example can be any folder but you *have* to use it's full path in the command and it must contain the result that was obtained by running the build for the  [Ceylon ZIP file](https://hub.docker.com/r/ceylon/ceylon-build/) first!
