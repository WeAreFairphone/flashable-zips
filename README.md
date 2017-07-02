Flashable ZIPs
===

This is a list of community flashable ZIPs from the [Fairphone Community](https://forum.fairphone.com) for a variety of devices.  
**Flashable ZIPs** are packages that can be flashed to Android devices, usually to extend the system. They need to be flashed by a custom recovery such as [TWRP](https://twrp.me/) or CWM Recovery.

This previously used to be a repository that contained the source for these packages, but each one has been moved to its respective repository.


List of flashable ZIPs
---

### microG Installer

| Repository | Latest release |
| ---------- | -------------- |
| [GitHub](https://github.com/WeAreFairphone/flashable-zip_microG) | [Download](https://github.com/WeAreFairphone/flashable-zip_microG/releases/latest) |

Install [microG](https://microg.org) or [UnifiedNlp](https://github.com/microg/android_packages_apps_UnifiedNlp/blob/master/README.md) into an Android system. Also includes an **OTA survival** `addon.d` script.  
You'll usually install them normally, but Google blocked userspace location providers in Android 7+, and some ROMs have not applied [required patches](https://github.com/microg/android_packages_apps_UnifiedNlp/tree/master/patches) yet, like LineageOS.

**microG** is a free-as-in-freedom re-implementation of [Google’s proprietary Android user space apps and libraries](https://arstechnica.com/gadgets/2013/10/googles-iron-grip-on-android-controlling-open-source-by-any-means-necessary/).  
**Unified Network Location Provider** (UnifiedNlp) is a library that provides Wi-Fi- and Cell-tower-based geolocation [with configurable plugins](https://github.com/microg/android_packages_apps_UnifiedNlp#usage) to applications that use Google’s network location provider. It is included in GmsCore but can also run independently on most Android systems.

### EmojiOne v2 Installer

| Repository | Latest release |
| ---------- | -------------- |
| [GitHub](https://github.com/WeAreFairphone/flashable-zip_emojione) | [Download](https://github.com/WeAreFairphone/flashable-zip_emojione/releases/latest) |

Replace Android [emoji set](https://www.google.com/get/noto/help/emoji/) with [EmojiOne](https://www.emojione.com/emoji/v2). Also includes an **OTA survival** `addon.d` script and saves a copy of the previous installed emoji on your device at `/system/fonts/NotoColorEmoji.ttf.old`.

**EmojiOne v2** is an emoji set more comprehensible than Android's one [before Marshmallow](http://blog.emojipedia.org/android-6-0-1-emoji-changelog/).  
Version 2 of EmojiOne is the last [open and free](https://github.com/Ranks/emojione/blob/2.2.7/LICENSE.md) version of EmojiOne. EmojiOne v3 and later are **not open** to the public anymore.

### Unroot FP2 Open

| Repository | Latest release |
| ---------- | -------------- |
| [GitHub](https://github.com/WeAreFairphone/flashable-zip_unroot) | [Download](https://github.com/WeAreFairphone/flashable-zip_unroot/releases/latest) |

Unroot Android. This was created originally as a clean way to unroot Fairphone 2 [Open OS](http://code.fairphone.com/projects/fp-osos/index.html#id2), that comes prerooted and with TWRP.

Removes `bin/su` and `xbin/su` binaries from `/system`, and some other configuration files if they exist.
Unrooting is needed to pass SafetyNet requirements for some apps. [Guide](https://forum.fairphone.com/t/pencil2-how-to-install-any-app-on-fp-open-os-for-beginners-and-experts/22516) and [motivation behind](https://forum.fairphone.com/t/how-to-be-able-to-install-and-use-any-app-on-fp-open-os-experimental/22327/34?u=roboe).


Install
---

Download a flashable ZIP from the above list.

Restart your device into recovery and start `ADB sideload`. Then run:
```sh
adb sideload <flashable-zip-name>
```

Alternatively, copy the resulting ZIPs to your device storage, restart your device into recovery and use the GUI `Install` or `Install ZIP` option.
