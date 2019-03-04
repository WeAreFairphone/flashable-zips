Index of Flashable ZIPs by the WeAreFairphone Community
===

This is an index of community flashable ZIPs from the [Fairphone Community](https://fairphone.community) for a variety of devices.  
**Flashable ZIPs** are packages that can be flashed to Android devices, usually to modify the software. They need to be flashed by a custom recovery such as [TWRP](https://twrp.me/) or CWM Recovery.

This previously used to be a repository that contained the source for these packages, but each one has been moved to its respective repository.


List of flashable ZIPs
---

### microG/UnifiedNlp Installer

| Repository | Latest release |
| ---------- | -------------- |
| [GitHub](https://github.com/WeAreFairphone/flashable-zip_microG) | [Download](https://github.com/WeAreFairphone/flashable-zip_microG/releases/latest) |

Install [microG](https://microg.org) or [UnifiedNlp](https://github.com/microg/android_packages_apps_UnifiedNlp/blob/master/README.md) into an Android system. Also includes an **OTA survival** `addon.d` script.  
You'll usually install them normally, but Google blocked userspace location providers in Android 7+, and some ROMs have not applied [required patches](https://github.com/microg/android_packages_apps_UnifiedNlp/tree/master/patches) yet, like LineageOS.

**microG** is a free-as-in-freedom re-implementation of [Google’s proprietary Android user space apps and libraries](https://arstechnica.com/gadgets/2013/10/googles-iron-grip-on-android-controlling-open-source-by-any-means-necessary/).  
**Unified Network Location Provider** (UnifiedNlp) is a library that provides Wi-Fi- and Cell-tower-based geolocation [with configurable plugins](https://github.com/microg/android_packages_apps_UnifiedNlp#usage) to applications that use Google’s network location provider. It is included in GmsCore but can also run independently on most Android systems.

### Noto Emoji Updater

| Repository | Latest release |
| ---------- | -------------- |
| [GitHub](https://github.com/WeAreFairphone/flashable-zip_noto-emoji) | [Download](https://github.com/WeAreFairphone/flashable-zip_noto-emoji/releases/latest) |

Update Android [emoji set](https://www.google.com/get/noto/help/emoji/) to the latest available, usually to the newest Android version. This also includes an OTA survival `addon.d` script and saves a copy of the previous installed emoji on your device at `/system/fonts/NotoColorEmoji.ttf.old`.

**Noto Emoji** is the emoji set used by the Android system and it currently supports all emoji defined in the latest Unicode version (v10.0). Font is availabe under the [SIL Open Font License, version 1.1](https://github.com/googlei18n/noto-emoji/blob/master/fonts/LICENSE).

### EmojiOne v2 Installer

| Repository | Latest release |
| ---------- | -------------- |
| [GitHub](https://github.com/WeAreFairphone/flashable-zip_emojione) | [Download](https://github.com/WeAreFairphone/flashable-zip_emojione/releases/latest) |

Replace Android [emoji set](https://www.google.com/get/noto/help/emoji/) with [EmojiOne](https://www.emojione.com/emoji/v2). Also includes an **OTA survival** `addon.d` script and saves a copy of the previous installed emoji on your device at `/system/fonts/NotoColorEmoji.ttf.old`.

**EmojiOne v2** is an emoji set more comprehensible than Android's one [before Marshmallow](http://blog.emojipedia.org/android-6-0-1-emoji-changelog/).  
Version 2 of EmojiOne is the last [open and free](https://github.com/Ranks/emojione/blob/2.2.7/LICENSE.md) version of EmojiOne. EmojiOne v3 and later are **not open** to the public anymore.

### Fairphone 2 `modem.zip`

| Repository | Latest release |
| ---------- | -------------- |
| [GitHub](https://github.com/WeAreFairphone/modem_zip_generator) | [Download](https://github.com/WeAreFairphone/modem_zip_generator/releases/latest) |

Update the proprietary firmware of your [Fairphone 2](https://shop.fairphone.com) to the latest available. Fairphone updates the software of the Fairphone 2 with [security patches](https://source.android.com/security/bulletin/) on a monthly basis.

### Unroot FP2 Open

| Repository | Latest release |
| ---------- | -------------- |
| [GitHub](https://github.com/WeAreFairphone/flashable-zip_unroot) | [Download](https://github.com/WeAreFairphone/flashable-zip_unroot/releases/latest) |

Unroot Android. This was created originally as a clean way to unroot Fairphone 2 [Open OS](http://code.fairphone.com/projects/fp-osos/index.html#id2) 5.1, that came prerooted and with TWRP.

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
