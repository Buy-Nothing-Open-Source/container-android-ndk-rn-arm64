FROM alpine:3.21 AS fetch
WORKDIR /opt/sdk

COPY alpine-aarch64.patch .

RUN apk add patch curl zip ninja cmake clang llvm lld llvm-libunwind-dev libatomic python3 icu-dev linux-headers \
    && curl -LO https://github.com/facebook/hermes/archive/refs/heads/rn/0.76-stable.zip \
    && unzip -q 0.76-stable.zip \
    && cd hermes-rn-0.76-stable \
    && patch -p1 < ../alpine-aarch64.patch \
    && cd .. \
    && cmake -S hermes-rn-0.76-stable -B hermes-build -G Ninja -DCMAKE_BUILD_TYPE=Release \
    && cmake --build ./hermes-build  \
    && mkdir hermes \
    && cp -r ./hermes-build/bin hermes/bin \
    && rm -rf hermes-rn-0.76-stable hermes-build 0.76-stable.zip alpine-aarch64.patch

