# Guide for AOSP commands `make`
To run this commands, exec `source build/envsetup.sh`
[See more info about build usage and concepts.](https://android.googlesource.com/platform/build/+/refs/heads/master/Usage.txt)
## Common targets
###### m help
    clean                   (aka clobber) equivalent to rm -rf out/
    installclean            Clean files installed from previous build. Use this when try re-build on another target, flavor.
    checkbuild              Build every module defined in the source tree
    droid                   Default target
    nothing                 Do not build anything, just parse and validate the build structure

    java                    Build all the java code in the source tree
    native                  Build all the native code in the source tree

    host                    Build all the host code (not to be run on a device) in the source tree
    target                  Build all the target code (to be run on the device) in the source tree

    (java|native)-(host|target)
    (host|target)-(java|native)
                            Build the intersection of the two given arguments

    snod                    Quickly rebuild the system image from built packages
                            Stands for "System, NO Dependencies"
    vnod                    Quickly rebuild the vendor image from built packages
                            Stands for "Vendor, NO Dependencies"
    pnod                    Quickly rebuild the product image from built packages
                            Stands for "Product, NO Dependencies"
    psnod                   Quickly rebuild the product_services image from built packages
                            Stands for "ProductServices, NO Dependencies"
    onod                    Quickly rebuild the odm image from built packages
                            Stands for "ODM, NO Dependencies"

## Targets
All target is declare on [main.mk](https://android.googlesource.com/platform/build/+/master/core/main.mk)
TODO: Write a tools copy all targets to the file txt

    dist
    dist_files
    ramdisk
    ramdisk_debug
    ramdisk_test_harness
    vendor_ramdisk_debug
    userdataimage
    cacheimage
    bptimage
    vendorimage
    vendorbootimage
    vendorbootimage_debug
    productimage
    systemextimage
    odmimage
    systemotherimage
    superimage_empty
    bootimage
    bootimage_debug
    bootimage_test_harness
    javac-check             Run all java compilations that use javac. use "javac-check-{target package}" to run java compilations only package.
    findbugs
    findlsdumps
    vbmetaimage
    apps_only               Only build apps and not the full system by default.
    update-api              
    clean-dex-files         Clean files rule in 'out' dir.
    droidcore               Build files and then package it into the rom formats.
    docs
## Module
###### List all module available
```bash
make modules
```
###### List common modules
    services                Build system services, output is file "services.odex"
    framework               Build all framework, output is folder "system"
    platform                Build java platform, this module include module framework above, output is file "platform.zip"
    sdk                     Build SDK, the lunch target must not be TARGET_BUILD_TYPE=debug. See https://android.googlesource.com/platform/sdk/+/master/docs/howto_build_SDK.txt

## ccache
Use for fast building aosp, about 35%.
The ccache have already removed on master, [see more](https://android-review.googlesource.com/c/platform/build/+/657884). But it's still can be used from local. But if facing error while buiding, disable the ccache.

###### Download ccache
- [Download ccache](https://github.com/my-android-platform/guide-aosp-building/tree/master/aosp_building/commands/make/ccache)

###### Set ccache size
```bash
ccache -M 10G
```

###### Claer ccache
```bash
ccache -C
```

###### Enable ccache
```bash
export USE_CCACHE=true   // set "false" to disable
export CCACHE_EXEC=/path/to/ccache
```
