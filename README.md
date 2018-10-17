# PE-Extended #

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/Extended-P/manifest -b pie

# Sync
repo sync -c -j8 --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash

# Setup Ccache
 # Use Ccache for faster building
 export USE_CCACHE=1
 export PATH="/usr/lib/ccache/:$PATH"
 prebuilts/misc/linux-x86/ccache/ccache -M 100G

# Set up environment
 . build/envsetup.sh

# Choose a target
 lunch aosp_$device-userdebug

# Build the code
 mka bacon -jX
```

