#FROM ekidd/rust-musl-builder AS builder

FROM rustlang/rust:nightly-stretch-slim AS builder

WORKDIR /project
COPY Cargo.toml ./
COPY src ./src
#RUN rustup target add x86_64-unknown-linux-musl && rustup install nightly
#RUN rustup target add --toolchain nightly x86_64-unknown-linux-musl
#RUN RUSTFLAGS='-C target-feature=+crt-static' cargo +nightly build --target x86_64-unknown-linux-musl

#ADD --chown=rust:rust . ./
#RUN rustup install nightly && cargo +nightly build --release

# # Bundle Stage
#FROM scratch
#COPY --from=builder /project/target/x86_64-unknown-linux-musl/release/mock-security-test .
#CMD ["./mock-security-test"]