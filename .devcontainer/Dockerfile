# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.202.5/containers/debian/.devcontainer/base.Dockerfile

# [Choice] Debian version (use bullseye or stretch on local arm64/Apple Silicon): bullseye, buster, stretch
ARG VARIANT="bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

#** [Optional] Uncomment this section to install additional packages. **
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends build-essential cmake netcat gdb meson rapidjson-dev libssl-dev doxygen pkg-config  python3 python3-distutils

RUN apt install -y libcurl4-openssl-dev

RUN git clone https://github.com/pistacheio/pistache.git /tmp/pistache-src  &&  \
    cd /tmp/pistache-src                                                    &&  \
    git checkout  cacd640d137cb412cf38acfe18ca27c4a09ea250                  &&  \
    ls -alh . && \
    meson setup build \
       --buildtype=release \
       -DPISTACHE_USE_SSL=true \
       -DPISTACHE_BUILD_EXAMPLES=true \
       -DPISTACHE_BUILD_TESTS=true \
       -DPISTACHE_BUILD_DOCS=false \
       --prefix="/usr/local"                                                && \
     meson compile -C build                                                 && \
     meson install -C build