# Pixel Experience #

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/PE-13/manifest.git -b thirteen-plus --depth=1 --git-lfs
```

```bash
# Sync
repo sync -c --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash
# Set up environment
. build/envsetup.sh
```

```bash
# Choose a target
lunch aosp_ginkgo-user
```

```bash
# Build the code
mka bacon -j$(nproc --all) | tee log.txt
```
