---
sidebar_label: 'Build from source'
sidebar_position: 4
---

# Why build from source
If you don't trust the official release builds hosted on GitHub, or if you want to make some modifications to the [source code](https://github.com/openbullet/OpenBullet2/) of OpenBullet 2, you might want to compile your own build instead of using a premade one.

# Prerequisites
Install the following
- [git](https://git-scm.com/downloads)
- [.NET 6 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)

:::info Info
Make sure to install the .NET 6 SDK and not the Runtime.
:::

# Building the Web Client from its source code
Open your favourite terminal (or git bash) and run

```bash
git clone https://github.com/openbullet/OpenBullet2/
```

now cd into the folder where `OpenBullet2.csproj` resides

```bash
cd OpenBullet2/OpenBullet2
```

and compile OB2 using

```bash
dotnet publish --configuration Release
```

you can then navigate to the publish folder and start OB2 with the usual command

```bash
cd bin/Release/net6.0/publish
dotnet ./OpenBullet2.dll
```

You should see some text like in the screenshot below

![Terminal Window](/img/installation/web-client/linux-terminal.png)

Now navigate to [http://127.0.0.1:5000](http://127.0.0.1:5000) using your favorite browser and you should see the setup page.

![Setup Page](/img/installation/web-client/setup-page.png)

# Building the Native Client from its source code (Windows only)
Open your favourite terminal (or git bash) and run

```bash
git clone https://github.com/openbullet/OpenBullet2/
```

now cd into the folder where `OpenBullet2.Native.csproj` resides

```bash
cd OpenBullet2/OpenBullet2.Native
```

and compile OB2 Native using

```bash
dotnet publish --configuration Release
```

you can then navigate to the publish folder (`bin/Release/net6.0/publish`) and double-click on `OpenBullet2.Native.exe` to run it.

You should now be able to see the application's homepage

![Home Page](/img/installation/native-client/home-page.jpg)