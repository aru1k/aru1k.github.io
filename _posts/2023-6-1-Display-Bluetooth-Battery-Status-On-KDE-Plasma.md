---
layout: post
title: Display Bluetooth Battery Status On KDE Plasma
published: true
---

KDE Plasma not showing bluetooth battery. And it's quite annoying when in the middle of work your bluetooth battery suddenly runs out. I experience it quite often.

Actually KDE Plasma has that feature but it's not enabled by default. This feature was introduced from KDE Plasma 5.15 Beta. Quoting from the [KDE official announcement](https://kde.org/announcements/plasma/5/5.14.90/):

> Bluetooth devices now show their battery status in the power widget. Note that this cutting-edge feature requires the latest versions of the upower and bluez packages.

I'm using KDE Plasma 5.27.5 for this guide. I think it will work if you have KDE Plasma 5.15 and above. Let's get to the guide.

1. First activate the bluetooth experimental feature with ```sudo nano /etc/bluetooth/main.conf```. Find "#Experimental = false", remove the # sign and change false to true. Save.
2. Restart bluetooth with ```sudo systemctl restart bluetooth```
3. Connect the bluetooth device and you will see the bluetooth device battery in the power widget.

That's all the guide. Hope that helps.

Credit to Reddit comment [@kocicak86](https://www.reddit.com/r/openSUSE/comments/xfkmzn/bluetooth_headphone_battery_level_in_kde/ip5qw3g/?context=3).