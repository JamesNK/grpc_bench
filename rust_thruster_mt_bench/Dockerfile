FROM rust:1.44.1-stretch

WORKDIR /app
COPY rust_thruster_mt_bench /app
COPY proto /app/proto

RUN rustup component add rustfmt --toolchain 1.44.1-x86_64-unknown-linux-gnu

RUN cat Cargo.toml
RUN cargo build --release
RUN cargo build --release

ENTRYPOINT cargo run --release
