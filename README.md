
# Motivation

<a href="https://gitpod.io/#https://github.com/wahabshah/pistache-cpp" rel="nofollow noopener noreferrer" target="_blank" class="after:hidden"><img src="https://gitpod.io/button/open-in-gitpod.svg" alt="Open in Gitpod"></a>

* This repository contains a server using [Pistache C++ framework](https://github.com/pistacheio/pistache)
  * [Documentation](https://wahabshah.github.io/pistache/)
* Pistache uses raw tcp/ip sockets
* Pistache does not support Windows yet
* Pistache’s has its own implementation of the [Promises/A+](https://promisesaplus.com/) standard available in many JavaScript implementations.

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
