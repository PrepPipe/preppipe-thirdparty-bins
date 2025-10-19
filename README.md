# Third-party binaries for PrepPipe

YOU SHOULD NEVER NEED TO TOUCH THIS REPO (unless you know what you are doing)

When packaging PrepPipe, the CI script would need to download third-party binaries (primarily `ffmpeg`) and add it into the package. Since the downloaded binaries can be different for each download, this creates unnecessary diff in the release package, increasing the wait time for even a small change. To fix this issue, we create this repo and we will cache all third-party binaries depended by the package here. In this way, the packing CI script will download dependencies cached here, ensuring minimal diff for release packages.

## Versioning
This repo will only have a "latest" release tag that contains the latest binaries. Refreshing the binaries should overwrite the previous tag.

To maintainer: Use the github action to trigger refreshing.
