# OpenJDK JRE Alpine Docker Image with Font Configuration Installed 

For applications requiring the use of Fonts, e.g Jasper Reports, fontconfig can't find any fonts in the java:8-jre-alpine image because there are no fonts. The Debian-based image has just enough fonts to support the default JDK fonts. These fonts come from the fonts-dejavu-core package, which is a transitive dependency of libfontconfig1 on Debian. The solution is to install the ttf-dejavu package in java:8-jre-alpine image

This docker image was created following the instructions on https://github.com/docker-library/openjdk/issues/73
