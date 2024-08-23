FROM ubuntu:24.10

RUN <<EOF1
cat > /etc/apt/sources.list.d/llvm-toolchain-noble-19.sources <<EOF2
Types: deb
URIs: http://apt.llvm.org/noble/
Suites: llvm-toolchain-noble-19
Components: main
EOF2
EOF1
RUN apt update --allow-insecure-repositories
RUN apt install -y cmake clang-19=1:19.1.0~++rc2-1~exp1 git libc++-19-dev=1:19.1.0~++rc2-1~exp1 ninja-build
RUN ln -s /usr/bin/clang++-19 /usr/bin/clang++
