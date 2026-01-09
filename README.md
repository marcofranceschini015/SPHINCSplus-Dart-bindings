## Overview

This repository provides Dart bindings for the SPHINCS+ post-quantum
signature scheme, implemented as a wrapper around the reference C++
implementation.

The goal is to make SPHINCS+ usable from Dart applications while
preserving the security properties of the original implementation.

## Why this project

Dart lacks native support for post-quantum signature schemes.
This project bridges that gap by exposing SPHINCS+ through a clean
and minimal Dart API, handling FFI boundaries, memory ownership,
and error propagation.

## Work in progress

This package is still in the early development phase, so it should not be considered as ready to use.

## Security considerations

- The cryptographic implementation is not reimplemented in Dart.
- All cryptographic operations rely on the original C++ code.
- The Dart layer only handles data marshaling and API exposure.

## Developer setup

Docker allows to develop using the same environment on different machines. First of all generate a docker_user.cfg file and write into it the username and the password of the user that will be created inside the container in the format user:password.

After that, to start the container run the following command:
```bash
bash setup.sh
```

Attach a Visual Studio Code window to the container and start develop!