

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.khulnasoft.com/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach_live**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>


If you have a pcap of a USB connection with a lot of Interruptions probably it is a USB Keyboard connection.

A wireshark filter like this could be useful: `usb.transfer_type == 0x01 and frame.len == 35 and !(usb.capdata == 00:00:00:00:00:00:00:00)`

It could be important to know that the data that starts with "02" is pressed using shift.

You can read more information and find some scripts about how to analyse this in:

* [https://medium.com/@ali.bawazeeer/kaizen-ctf-2018-reverse-engineer-usb-keystrok-from-pcap-file-2412351679f4](https://medium.com/@ali.bawazeeer/kaizen-ctf-2018-reverse-engineer-usb-keystrok-from-pcap-file-2412351679f4)
* [https://github.com/tanc7/HacktheBox\_Deadly\_Arthropod\_Writeup](https://github.com/tanc7/HacktheBox_Deadly_Arthropod_Writeup)



<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.khulnasoft.com/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach_live**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>


