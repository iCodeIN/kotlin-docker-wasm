# Kotlin Wasm With Docker

Kotlin `1.8.0-Beta` and Docker `4.15` support Wasm, but the support is experimental.

## Requirements

1. Install Docker Desktop 4.15

## Building

1. `./gradlew build`
1. `docker buildx build --platform wasi/wasm32 -t hello-wasm-kotlin .`

## Running

1. `docker run --runtime=io.containerd.wasmedge.v1 --platform=wasi/wasm32 hello-wasm-kotlin`
