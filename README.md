# Guide for buiding AOSP, porting device, android platform, hardware abstract layer.

This guide using for personal purposes.

## Google communication group

- [Android Building](https://groups.google.com/forum/#!forum/android-building): Discussion of building the AOSP platform distribution from source without modification for AOSP-supported build targets.
- [Android Porting](https://groups.google.com/forum/#!forum/android-porting): For technical discussion of porting the AOSP distribution from source to non-AOSP-supported build targets, and porting-related modifications to AOSP distribution for customization.
- [Android Platform](https://groups.google.com/forum/#!forum/android-platform): For technical discussion of the internals of the AOSP distribution

## Hardware requirement

```bash
1. OS: Ubuntu LTS 64-bit (12.04 LTS, 14.04 LTS, 18.04 LTS)
2. RAM: At least 16 GB
3. CPU: i3 or above with 6 core 6 thread or more.
4. At least 250GB of free disk space to check out the code and an extra 150 GB to build it. If you conduct multiple builds, you need additional space.
```

**Reference:** [Hardware requirement](https://source.android.com/setup/build/requirements)

## Download AOSP

**Reference:**
[Establishing a Build Environment](https://source.android.com/setup/build/initializing)
[Downloading](https://source.android.com/setup/build/downloading)

###### Download Repo

```bash
mkdir ~/bin
PATH=~/bin:$PATH
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo
```

###### Download Source

```bash
repo init -u https://android.googlesource.com/platform/manifest -b branch
repo sync
```

## Topic

1. [Repo (commands, version and issues).](https://github.com/my-android-platform/guide-aosp-building/tree/master/repo)
2. [AOSP Building (commands, description modules, issues).](https://github.com/my-android-platform/guide-aosp-building/tree/master/aosp_building)
3. [Android platform.](https://github.com/my-android-platform/guide-aosp-building/tree/master/android_platform)
4. [Hardware abstract layer.](https://github.com/my-android-platform/guide-aosp-building/tree/master/hal)
5. [Kernel.](https://github.com/my-android-platform/guide-aosp-building/tree/master/kernel)