FROM quay.io/curl/curl AS installer
RUN curl -L https://dot.net/v1/dotnet-install.sh -o /usr/bin/install-dotnet \
    && chmod +x /usr/bin/install-dotnet

FROM __hive__/base-deployment:v1
USER 0
RUN apt-get update -y \
    && apt-get install -y \
        libc6 \
        libgcc-s1 \
        libicu74 \
        liblttng-ust1 \
        libssl3 \
        libstdc++6 \
        zlib1g \
    && rm -rf /var/lib/apt/lists/*
COPY --from=installer /usr/bin/install-dotnet /usr/bin/install-dotnet
ARG DOTNET_SDK_CHANNEL_VERSION
RUN install-dotnet --runtime --channel "${DOTNET_SDK_CHANNEL_VERSION}" --install-dir /usr/share/dotnet \
    && ln -s /usr/share/dotnet/dotnet /usr/local/bin/dotnet

USER 1000
