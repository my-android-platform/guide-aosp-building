# Guide for AOSP commands
To run these commands bellow, exec `source build/envsetup.sh`
## Common commands
- **`lunch`**:      lunch <product_name>-<build_variant> Selects <product_name> as the product to build, and <build_variant> as the variant to build, and stores those selections in the environment to be read by subsequent invocations of 'm' etc.
- **`tapas`**:      tapas [<App1> <App2> ...] [arm|x86|mips|arm64|x86_64|mips64] [eng|userdebug|user]
- **`croot`**:      Changes directory to the top of the tree, or a subdirectory thereof.
- **`m`**:          Makes from the top of the tree.
- **`mm1`**:        Builds all of the modules in the current directory, but not their dependencies.
- **`mmm`**:        Builds all of the modules in the supplied directories, but not their dependencies. To limit the modules being built use the syntax: `mmm dir/:target1,target2`.
- **`mma`**:        Builds all of the modules in the current directory, and their dependencies.
- **`mmma`**:       Builds all of the modules in the supplied directories, and their dependencies.
- **`provision`**:  Flash device with all required partitions. Options will be passed on to fastboot.
- **`cgrep`**:      Greps on all local C/C++ files.
- **`ggrep`**:      Greps on all local Gradle files.
- **`jgrep`**:      Greps on all local Java files.
- **`resgrep`**:    Greps on all local res/*.xml files.
- **`mangrep`**:    Greps on all local AndroidManifest.xml files.
- **`mgrep`**:      Greps on all local Makefiles files.
- **`sepgrep`**:    Greps on all local sepolicy files.
- **`sgrep`**:      Greps on all local source files.
- **`godir`**:      Go to the directory containing a file.
- **`allmod`**:     List all modules. Must call `refreshmod` before use it.
- **`gomod`**:      Go to the directory containing a module. Must call `refreshmod` before use it.
- **`pathmod`**:    Get the directory containing a module.
- **`refreshmod`**: Refresh list of modules for `allmod/gomod`.