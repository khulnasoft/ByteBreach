# Android Forensics

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.bytebreach.xyz/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach\_live**](https://twitter.com/bytebreach\_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>

## Locked Device

To start extracting data from an Android device it has to be unlocked. If it's locked you can:

* Check if the device has debugging via USB activated.
* Check for a possible [smudge attack](https://www.usenix.org/legacy/event/woot10/tech/full\_papers/Aviv.pdf)
* Try with [Brute-force](https://www.cultofmac.com/316532/this-brute-force-device-can-crack-any-iphones-pin-code/)

## Data Adquisition

Create an [android backup using adb](../mobile-pentesting/android-app-pentesting/adb-commands.md#backup) and extract it using [Android Backup Extractor](https://sourceforge.net/projects/adbextractor/): `java -jar abe.jar unpack file.backup file.tar`

### If root access or physical connection to JTAG interface

* `cat /proc/partitions` (search the path to the flash memory, generally the first entry is _mmcblk0_ and corresponds to the whole flash memory).
* `df /data` (Discover the block size of the system).
* dd if=/dev/block/mmcblk0 of=/sdcard/blk0.img bs=4096 (execute it with the information gathered from the block size).

### Memory

Use Linux Memory Extractor (LiME) to extract the RAM information. It's a kernel extension that should be loaded via adb.

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.bytebreach.xyz/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach\_live**](https://twitter.com/bytebreach\_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>