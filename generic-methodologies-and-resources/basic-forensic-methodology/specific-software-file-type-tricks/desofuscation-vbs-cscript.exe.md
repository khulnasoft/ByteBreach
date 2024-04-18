

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.bytebreach.xyz/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach_live**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>


Some things that could be useful to debug/deobfuscate a malicious VBS file:

## echo

```bash
Wscript.Echo "Like this?"
```

## Commnets

```bash
' this is a comment
```

## Test

```bash
cscript.exe file.vbs
```

## Write data to a file

```js
Function writeBinary(strBinary, strPath)

    Dim oFSO: Set oFSO = CreateObject("Scripting.FileSystemObject")

    ' below lines purpose: checks that write access is possible!
    Dim oTxtStream

    On Error Resume Next
    Set oTxtStream = oFSO.createTextFile(strPath)

    If Err.number <> 0 Then MsgBox(Err.message) : Exit Function
    On Error GoTo 0

    Set oTxtStream = Nothing
    ' end check of write access

    With oFSO.createTextFile(strPath)
        .Write(strBinary)
        .Close
    End With

End Function
```



<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.bytebreach.xyz/courses/arte"><strong>htARTE (ByteBreach AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support ByteBreach:

* If you want to see your **company advertised in ByteBreach** or **download ByteBreach in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/khulnasoft)!
* Get the [**official PEASS & ByteBreach swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@bytebreach_live**](https://twitter.com/bytebreach_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**ByteBreach**](https://github.com/khulnasoft/bytebreach) and [**ByteBreach Cloud**](https://github.com/khulnasoft/bytebreach-cloud) github repos.

</details>


