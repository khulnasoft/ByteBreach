

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.khulnasoft.com/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach_live**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>


If you have pcap with data being **exfiltrated by DNSCat** (without using encryption), you can find the exfiltrated content.

You only need to know that the **first 9 bytes** are not real data but are related to the **C\&C communication**:

```python
from scapy.all import rdpcap, DNSQR, DNSRR
import struct 

f = ""
last = ""
for p in rdpcap('ch21.pcap'):
	if p.haslayer(DNSQR) and not p.haslayer(DNSRR):

		qry = p[DNSQR].qname.replace(".jz-n-bs.local.","").strip().split(".")
		qry = ''.join(_.decode('hex') for _ in qry)[9:]
		if last != qry:
			print(qry)
			f += qry
		last = qry

#print(f)
```

For more information: [https://github.com/jrmdev/ctf-writeups/tree/master/bsidessf-2017/dnscap](https://github.com/jrmdev/ctf-writeups/tree/master/bsidessf-2017/dnscap)\
[https://github.com/iagox86/dnscat2/blob/master/doc/protocol.md](https://github.com/iagox86/dnscat2/blob/master/doc/protocol.md)


There is a script that works with Python3: [https://github.com/josemlwdf/DNScat-Decoder](https://github.com/josemlwdf/DNScat-Decoder)

```
python3 dnscat_decoder.py sample.pcap bad_domain
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


