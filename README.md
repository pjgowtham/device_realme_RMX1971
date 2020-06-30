# android_device_realme_RMX1971
For building Orangefox for Realme 5 pro

Orangefox device tree for Realme 5 pro

## Features

Works:

- Everything

## Compile

First checkout manifest :

```
repo init --depth=1 -u https://gitlab.com/OrangeFox/Manifest.git -b fox_9.0
repo sync
```

Then add these projects to .repo/manifest.xml:

```xml
<project path="device/realme/RMX1971" name="device/RMX1971" remote="gitlab" revision="master" />
```

Finally execute these:

```
. build/envsetup.sh
lunch omni_RMX1971-eng
mka recoveryimage ALLOW_MISSING_DEPENDENCIES=true
```

To test it:

```
fastboot flash /path/to/recovery.img
and then
Flash the zip through the recovery for addon support.
```


## Thanks

- Thanks to @mauronfrio for the TWRP trees
