# FZ - 125kHz RFID

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.bytebreach.xyz/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@khulnasoftm**](https://twitter.com/bytebreach\_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>

<figure><img src="/.gitbook/assets/WebSec_1500x400_10fps_21sn_lightoptimized_v2.gif" alt=""><figcaption></figcaption></figure>

{% embed url="https://websec.nl/" %}


## Intro

For more info about how 125kHz tags work check:

{% content-ref url="../pentesting-rfid.md" %}
[pentesting-rfid.md](../pentesting-rfid.md)
{% endcontent-ref %}

## Actions

For more info about these types of tags [**read this intro**](../pentesting-rfid.md#low-frequency-rfid-tags-125khz).

### Read

Tries to **read** the card info. Then it can **emulate** them.

{% hint style="warning" %}
Note that some intercoms try to protect themselves from key duplication by sending a write command prior to reading. If the write succeeds, that tag is considered fake. When Flipper emulates RFID there is no way for the reader to distinguish it from the original one, so no such problems occur.
{% endhint %}

### Add Manually

You can create **fake cards in Flipper Zero indicating the data** you manually and then emulate it.

#### IDs on cards

Some times, when you get a card you will find the ID (or part) of it written in the card visible.

* **EM Marin**

For example in this EM-Marin card in the physical card is possible to **read the last 3 of 5 bytes in clear**.\
The other 2 can be brute-forced if you cannot read them from the card.

<figure><img src="../../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

* **HID**

Same happens in this HID card where only 2 out of 3 bytes can be found printed in the card

<figure><img src="../../../.gitbook/assets/image (1011).png" alt=""><figcaption></figcaption></figure>

### Emulate/Write

After **copying** a card or **entering** the ID **manually** it's possible to **emulate** it with Flipper Zero or **write** it in a real card.

## References

* [https://blog.flipperzero.one/rfid/](https://blog.flipperzero.one/rfid/)

<figure><img src="/.gitbook/assets/WebSec_1500x400_10fps_21sn_lightoptimized_v2.gif" alt=""><figcaption></figcaption></figure>

{% embed url="https://websec.nl/" %}


<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.bytebreach.xyz/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@khulnasoftm**](https://twitter.com/bytebreach\_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>
