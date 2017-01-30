# ScreenSquid packaged for Linux

[Site](screensquid-linux.nicosantangelo.com)

## Download my pre-packaged version

[ia32](https://github.com/NicoSantangelo/screensquid-linux/releases/download/1.0.0/Screensquid-linux-ia32.zip)
[x64](https://github.com/NicoSantangelo/screensquid-linux/releases/download/1.0.0/Screensquid-linux-x64.zip)
[armv7l](https://github.com/NicoSantangelo/screensquid-linux/releases/download/1.0.0/Screensquid-linux-armv7l.zip)

## Create your own

You'll need to have [`asar`](https://www.npmjs.com/package/asar) and [`electron-packager`](https://github.com/electron-userland/electron-packager) installed

- Get your hands on the app contents. You could try installing it on a Windows/Mac VM or in a borrowed computer
- Find the `app.asar` and `electron.asar` files, usually under the `Resources` folder

```bash
$ mkdir app
$ asar extract app.asar app
$ asar extract electron.asar app
$ cd app && npm i && cd ..
$ electron-packager app Screensquid --platform=linux --arch=x64 # (ia32, x64, armv7l)
```

- You're done! :tada:
