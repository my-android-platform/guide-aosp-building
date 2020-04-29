# Guide for AOSP commands `make`
To run this commands, exec `source build/envsetup.sh`
[See more info about build usage and concepts.](https://android.googlesource.com/platform/build/+/refs/heads/master/Usage.txt)
## Common goals
    clean                   (aka clobber) equivalent to rm -rf out/
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

## ccache
Use for fast building aosp.
The ccache have already removed on master, but it's still can be used from local. But if facing error while buiding, disable the ccache.

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