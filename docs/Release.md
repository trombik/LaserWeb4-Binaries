# Releasing

[A GitHub Action workflow](../.github/workflows/release.yml) automatically
builds a git ref when:
drafts a release when the followings are met:

- A pull request has been created or a branch is pushed

And it drafts a release when the followings are met:
- All builds for targets are successfully built
- The ref has a tag with "v\*"
- If the tag ends with "-pre", the release will be pre-release

## Requirements

To test `AppImage` binary on bare-minimum Ubuntu 18.04 `virtualbox` VM, the
following packages must be installed.

```console
> apt-get install libgtk-3-0 libx11-xcb1 libnss3 libasound2 libdbus-glib-1-2
```

In addition, to run the `AppImage` binary, X and an window manager must be
installed.

```console
> apt-get install lightgdm virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11
```
