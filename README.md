
# Gengkapak Project twelve

## Building Gengkapak Project
### Create a directory
```
 mkdir -p ~/gkp
 cd ~/gkp
```

### Initialize Gengkapak Project Source manifest in the directory
```
 repo init -u https://github.com/GengKapak-Project/platform_manifest.git -b twelve
 repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
```

### Now, let's start compilation

```
 source build/envsetup.sh
 lunch gengkapak_<device_codename>-userdebug
 make kapak -j$(nproc --all)
```