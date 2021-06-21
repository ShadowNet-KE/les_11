FROM alpine:3.13

# Install package version
ENV PKG_JDK=openjdk11-jdk
ENV PKG_MVN=maven<3.6.3-r1

RUN apk add docker \
    && apk add git \
    && apk add ${PKG_JDK} \
    && apk add ${PKG_MVN}