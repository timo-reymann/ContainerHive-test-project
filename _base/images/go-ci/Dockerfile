FROM __hive__/base-ci:v1
# Install golang
ARG GOLANG_VERSION
ENV PATH="/usr/local/go/bin:$PATH"
RUN curl -L https://go.dev/dl/go${GOLANG_VERSION}.linux-amd64.tar.gz | tar -xz -C /usr/local

# Install zig
ARG ZIG_VERSION
RUN curl -L https://ziglang.org/builds/zig-linux-x86_64-${ZIG_VERSION}.tar.xz | tar -xJ -C /usr/local
ENV PATH="/usr/local/zig-linux-x86_64-0.11.0:$PATH"