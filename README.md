# Android NDK with React Native for ARM64

This repository provides containers to build and run React Native projects using a linux/arm64 container.
The current release targets React Native 0.76.

Target audience:
- Mac users running podman or docker
- Cloud builds using arm64
- Upstream developers from Google and Meta

Changes:
- Patches for Hermes for compatibility with musl

Ideally this repository will be archived, as changes make it upstream and arm64 becomes supported by the Android NDK and React Native projects.

For dependencies and details, consult the source code.

## License

This repository is authored by The Buy Nothing Project and released under CC0 where available.
Where not available, this release falls back to a choice of Apache 2.0 or MIT license.

Note this project relies on a myriad of other licenses to operate. 
The [@lzhiyong/android-sdk-tools](https://github.com/lzhiyong/android-sdk-tools/), for example, is licensed under the Apache 2.0 license.


## Thanks

- Thanks to @lzhiyong for static cmake builds of android-sdk-tools
- Thanks to the enormous ecosystem React Native is built upon 


