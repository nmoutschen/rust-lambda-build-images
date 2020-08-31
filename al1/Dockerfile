FROM amazon/aws-sam-cli-build-image-provided

ENV RUSTUP_HOME=/usr/local/rustup \
    RUST_ARCH=x86_64-unknown-linux-gnu \
    CARGO_HOME=/usr/local/cargo \
    PATH=/usr/local/cargo/bin:$PATH \
    RUST_VERSION=1.46.0

RUN curl https://static.rust-lang.org/rustup/dist/${RUST_ARCH}/rustup-init -o rustup-init ; \
    chmod +x rustup-init ; \
    ./rustup-init -y --default-toolchain $RUST_VERSION --default-host $RUST_ARCH ; \
    chmod -R a+w $RUSTUP_HOME $CARGO_HOME ; \
    rustup --version; \
    cargo --version; \
    rustc --version;
