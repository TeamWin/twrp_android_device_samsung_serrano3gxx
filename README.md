## TWRP device tree for Samsung Galaxy S4 Mini (International 3G)
## serrano3g, serrano3gxx

Add to `.repo/local_manifests/serrano3gxx.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project name="LineageOS/android_device_qcom_common" path="device/qcom/common" remote="github" revision="cm-14.1" />
  <project name="LineageOS/android_kernel_samsung_msm8930-common" path="kernel/samsung/msm8930-common" remote="github" revision="cm-14.1" />
  <project name="ripee/twrp_android_device_samsung_serrano3gxx" path="device/samsung/serrano3gxx" remote="github" revision="android-7.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_serrano3gxx-eng
mka recoveryimage
```

