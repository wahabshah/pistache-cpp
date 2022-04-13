
# Motivation

<a href="https://gitpod.io/#https://github.com/wahabshah/pistache-cpp" rel="nofollow noopener noreferrer" target="_blank" class="after:hidden"><img src="https://gitpod.io/button/open-in-gitpod.svg" alt="Open in Gitpod"></a>

* This repository contains a server using [Pistache C++ framework](https://github.com/pistacheio/pistache)
* This framework uses raw tcp/ip sockets

## Build Echo Server Iteration1
```sh
rm -rf build && mkdir -p build && \
(cd build && cmake -DCMAKE_BUILD_TYPE=Debug .. && make clean all VERBOSE=1) && \
./build/PistacheProject
```

```sh
curl http://localhost:9080
Hello World!
```

# Links

```sh
stretch 
Meson version is 0.37.1 but project requires >=0.50.0.

```