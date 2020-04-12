# This image is based on net core runtime-deps
# Can only be used by self contained builds
FROM mcr.microsoft.com/dotnet/core/runtime-deps:3.1
RUN \
    apt update \
    \
    && apt install -y --no-install-recommends  \
    ca-certificates=20190110 \
    nano=3.2-3 \
    bash=5.0-4 \
    wget=1.20.1-1.1 \
    git=1:2.20.1-2+deb10u1 \
    \
    && rm -fr \
    /tmp/* \
    /var/{cache,log}/* \
    /var/lib/apt/lists/*


COPY install-s6.sh /install-s6.sh
RUN chmod +x /install-s6.sh
RUN /install-s6.sh
