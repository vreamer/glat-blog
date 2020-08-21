---
title: "Use Bluestacks 4 to run Android apps with Flutter on Mac"
date: 2020-08-21T14:06:37+08:00
---

### Why I wanted to switch to Bluestacks 4

I started off using Android Emulators from Android Virtual Device (AVD) Manager. However, with the extra memory and CPU consumption from the emulator, my development speed really took a hit. Especially when I try to utilize the hot reload feature from Flutter, it takes several seconds to load the changes and heat up my computer at the same time.

Hence, I was looking for a slimmer and faster emulator alternative. After some [research](https://www.androidauthority.com/best-android-emulators-for-pc-655308/), I narrowed down to BlueStacks. Now the hot reload is almost instant and my computer stays cool while doing it.

But compared to using Android Emulators from AVD. There are some extra configurations to help Flutter detect Bluestacks as a runnable device. These configurations should be similar if you choose other Android Emulators. In this blog, we will use Bluestacks as an example to make Flutter detect your emulators.

### Tools

1. Flutter
   ![Flutter Version](https://i.imgur.com/r7yVCG3.png?2)

2. BlueStacks 4

![BlueStacks Version 4](https://i.imgur.com/fWzT5La.png?1)

### Steps

The third step is optional. You can skip if your emulator works fine after the first two steps.

1. Install BlueStacks

Install BlueStacks from [here](https://www.bluestacks.com/). For Mac users, if you run into security setting issues. You can refer to this [blog](https://support.bluestacks.com/hc/en-us/articles/360000736632-How-can-I-Install-and-launch-BlueStacks-on-Mac-OS-).

After the BlueStacks Emulator is up and running, we can run `flutter devices` At this moment, Flutter cannot find the BlueStacks Emulator. That's because we haven't turn on the debug mode.

![No Devices](https://i.imgur.com/WT0gNWa.png)

2. Enable Android Debug Bridge (ADB)

Go to `BlueStacks >> Preferences >> Preferences`

Check the `Enable Android Debug Bridge (ADB)` option

![Enable ADB](https://i.imgur.com/vPKEx3d.png?1)

Try to run `flutter devices` again. At this point, you should see BlueStacks Emulator listed under flutter devices. 
![Devices connected](https://i.imgur.com/rR79yzU.png?1)

If the BlueStacks Emulator is not present, proceed to the next step.

3. (Optional) Connect with ADB

The BlueStacks Emulator is running on port 5555. Connect manually with adb

```
adb connect localhost:5555
```

![Connect manually](https://i.imgur.com/jHM6NFI.png)

Lastly, run `flutter devices` again to confirm the BlueStacks Emulator is detected.

Now `flutter run` will install the apk on the BlueStacks Emulator.

| App                                                            |                           Installed                            |
| -------------------------------------------------------------- | :------------------------------------------------------------: |
| ![APK deployed to BlueStacks](https://i.imgur.com/b1GqxmH.png) | ![APK deployed to BlueStacks](https://i.imgur.com/0saCOvK.png) |

Voilà. Have fun coding :)


### Reference:
* [How to connect flutter to Bluestacks emulator?](https://stackoverflow.com/questions/55878399/how-to-connect-flutter-to-bluestacks-emulator)