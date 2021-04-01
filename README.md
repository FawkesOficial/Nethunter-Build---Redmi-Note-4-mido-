# Nethunter Build - Redmi Note 4(mido)
I'm making this repo for two reasons:
* Help someone else that fell into the same assle that I did
* Keep a guide for myself in case I ever want to re-install/fix a Nethunter Build for mido

I also want to say upfront that I take no credit other than the fact that I'm compiling everyhing into this repo. All the credit goes to [this guy on XDA](https://forum.xda-developers.com/m/uspdsr.7758199/) that gave the full solution that ended up working for me.

Im so glad I found that post buried in the Kernel thread. Without it I probably would have been stuck for ages. My problem was that I was actually trying to install the kernel in a "treble" ROM.

At the time I'm writing this repo(01/04/2021), it was kind of hard to find an actual good, working, and most importantly, non-treble ROM. I ended up going with Liquid Remix like the guy mentioned in the post and tbh I recomend going with that aswell.

If you have any questions, feel free to open an Issue or contact me on Twitter [@FawkesOficial](https://twitter.com/FawkesOficial)
## Instalation Steps:
These instalation steps are based [on this post](https://forum.xda-developers.com/t/kernel-nethunter-oreo-for-mido.3768887/post-77992244) from the [Kernel's XDA thread](https://forum.xda-developers.com/t/kernel-nethunter-oreo-for-mido.3768887/).

1. Boot into Recovery mode. (*I used OrangeFox. More on that later.*)
2. Wipe everything. (*Apart from usb-otg and micro-sd. You might not need to do this but I totaly recomend you to do so*)
3. Flash an Android **8.1.0, non-treble** ROM (*Example: Liquid Remix 9.0.8*)
4. Flash Magisk.
5. Flash GApps.
6. Wipe Cache and Dalvik.
7. Reboot into System.
8. Go trough the usual Android setup.
9. Install the Magisk App.
10. Inside the Magisk App, search for the Busybox Addon and then install it.
11. Reboot into Recovery.
12. Flash the Kernel "nethunter-mido-oreo-kalifs-full-v1.0.zip". This can take a couple of minutes.
13. Unfortunately, this doesn't automatically install all the apps. To proceed and install the rest of the apps, go to [store.nethunter.com](https://store.nethunter.com), download and install the Nethunter Store app.
14. Search and Install:
* NetHunter
* NetHunter Terminal
* USB Keyboard
* NetHunter KeX
15. Open the NetHunter App 🡒 ≡ 🡒 Kali Chroot Manager; and finally press 'START KALI CHROOT'
16. You are done !

## Troubleshooting:
I really recomend you to take a look at these steps aswell because chances are that you will probably fall into these problems too.

#### apt-get update KEYEXPIRED:
Fix: Open NetHunter Terminal 🡒 Select: Kali 🡒 Run: `wget -q -O - https://archive.kali.org/archive-key.asc | apt-key add`

#### KeX Manager not properly starting the server:
Fix: Open NetHunter Terminal 🡒 Select: Kali 🡒 Run: `apt-get update && apt-get full-upgrade -y`

#### DeAuth 🡒 'SCAN NETWORKS' not showing any output + Possibly other modules not working:
Fix: Download the latest 'nh_files' folder from https://gitlab.com/kalilinux/nethunter/apps/kali-nethunter-app/-/tree/master/assets/nh_files
<img src="https://user-images.githubusercontent.com/45067011/113225936-d7e03480-9286-11eb-9d17-5ba12b5ba283.png" width="600" height="280"/>
🡒 Open your desired file explorer 🡒 Internal Storage 🡒 Replace the 'nh_files' folder with the one you downloaded and extracted from the website.\
\* *For extracting .zip and .rar files you can install 'RAR' app from Google Play Store*

#### NetHunter App 🡒 DuckHunter HID not converting STRING's:
Fix: Unfortunately, as of 01/04/2021, the NetHunter App's DuckHunter HID Converter does not convert STRING's into shell scripts that can be run.
Because of this I've made two repositories to attempt to fix this.\
I recomend you use this one [FawkesOficial/duckhunter](https://github.com/FawkesOficial/duckhunter) wich is a fork of the original DuckHunter repo by @byt3bl33d3r\
\* *Run it from the Kali shell!*

## Original Downloads:
- Recovery: [OrangeFox-mido-stable@R11.0](https://orangefox.download/device/mido)
- ROM: [Liquid Remix-9.0.8-20180317-Official_Nikhil-mido](https://androidfilehost.com/?fid=962187416754468620)
- Kernel: [kernel-nethunter-oreo-for-mido](https://forum.xda-developers.com/t/kernel-nethunter-oreo-for-mido.3768887/)
- Magisk: Magisk-v22.0 - [Download Latest](https://magiskmanager.com/downloading-magisk-manager)
- GApps: ARM64 --> 8.1 --> pico - [Download Page](https://opengapps.org/)
- [Nethunter Store](https://store.nethunter.com)
- ['nh_files' folder](https://gitlab.com/kalilinux/nethunter/apps/kali-nethunter-app/-/tree/master/assets/nh_files)
