# Skeleton Key

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.khulnasoft.com/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@khulnasoftm**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>

## Skeleton Key Attack

The **Skeleton Key attack** is a sophisticated technique that allows attackers to **bypass Active Directory authentication** by **injecting a master password** into the domain controller. This enables the attacker to **authenticate as any user** without their password, effectively **granting them unrestricted access** to the domain.

It can be performed using [Mimikatz](https://github.com/gentilkiwi/mimikatz). To carry out this attack, **Domain Admin rights are prerequisite**, and the attacker must target each domain controller to ensure a comprehensive breach. However, the attack's effect is temporary, as **restarting the domain controller eradicates the malware**, necessitating a reimplementation for sustained access.

**Executing the attack** requires a single command: `misc::skeleton`.

## Mitigations

Mitigation strategies against such attacks include monitoring for specific event IDs that indicate the installation of services or the use of sensitive privileges. Specifically, looking for System Event ID 7045 or Security Event ID 4673 can reveal suspicious activities. Additionally, running `lsass.exe` as a protected process can significantly hinder attackers' efforts, as this requires them to employ a kernel mode driver, increasing the attack's complexity.

Here are the PowerShell commands to enhance security measures:

- To detect the installation of suspicious services, use: `Get-WinEvent -FilterHashtable @{Logname='System';ID=7045} | ?{$_.message -like "*Kernel Mode Driver*"}`

- Specifically, to detect Mimikatz's driver, the following command can be utilized: `Get-WinEvent -FilterHashtable @{Logname='System';ID=7045} | ?{$_.message -like "*Kernel Mode Driver*" -and $_.message -like "*mimidrv*"}`

- To fortify `lsass.exe`, enabling it as a protected process is recommended: `New-ItemProperty HKLM:\SYSTEM\CurrentControlSet\Control\Lsa -Name RunAsPPL -Value 1 -Verbose`

Verification after a system reboot is crucial to ensure that the protective measures have been successfully applied. This is achievable through: `Get-WinEvent -FilterHashtable @{Logname='System';ID=12} | ?{$_.message -like "*protected process*`

## References
* [https://blog.netwrix.com/2022/11/29/skeleton-key-attack-active-directory/](https://blog.netwrix.com/2022/11/29/skeleton-key-attack-active-directory/)

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.khulnasoft.com/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@khulnasoftm**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>
