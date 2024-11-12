# FCPS Tech exploits
A list of functioning offline downloads for all of the stuff on my website after it got blocked, as well as instructions for bypassing consorship and jailbreaking school computers in FCPS.

### Disclaimer
~~Sh1mmer will probably not be working on FCPS chromebooks. You will probably need some way to bypass the Fog or the Tsunami, as the chromebooks use ChromeOS 128.~~

Sh1mmer works on FCPS chromebooks ONLY with the Ti50 version of the Pencil Bypass. View the writeup [here](https://github.com/catfoolyou/Block-Bypass/blob/main/pencilbypass-ti50.md)
These hacks might not work on computers outside of FCPS because every district and/or county uses different software and hardware.

Shimboot ~~is currently being tested~~ works.

# WARNING
FCPS no longer gives out windows laptops to everyone. The previously working methods have been patched on their course specific windows PCs and most likely on the personal windows laptops as well.

CS students are now given access to personal windows laptops instead of chromebooks, but again they will need to be flashed and have their BIOS passwords reset so as to reinstall the OS. 

# Chromebooks
Most people at FCPS have been switched to chromebooks, which are much harder to jailbreak than to old Windows laptops. 
~~The easiest way to crack FCPS chromebooks would be via [this method](https://github.com/CaenJones/Chromebook-Testing/blob/main/README.md) (Mirror available [here](https://github.com/catfoolyou/Block-Bypass/blob/main/Chromebooks.md) in case the site gets taken down or it's blocked.)~~

## Downgrading kernel versions (kernver)

To prevent most exploits being patched, you can downgrade both chrome version and kernver to something manageable.

Use KVS, with a full writeup and instructions available here: https://github.com/kxtzownsu/KVS

Get images from chrome100.dev

G11 Chromebook: `nissa`

G10 Chromebook: `dedede`

Full instructions are available here: https://chrome100.dev/guide

## Sh1mmer
As of September 16th (2024 I think), sh1mmer with the tsunami bypass has been confirmed working with ChromeOS r128. This exploit allows for unenrollment and the ability to switch into developer mode, plus other things.

FCPS Chromebooks come in two models - HP Fortis G10 and G11. You can check this on the underside of the chromebook, which will usually be under the FCPS barcode (this varies from school to school).

G11 Chromebook: `nissa`

G10 Chromebook: `dedede`

Full writeup is available here: https://github.com/catfoolyou/Block-Bypass/blob/main/shimmer.md

## Shimboot
Shimboot is an exploit based on sh1mmer that boots a linux distribution off a USB or a spoofed unenrolled chromeOS. It works because the rootfs of the shim (a recovery image) is not verified, meaning that it can be replaced with whatever else.

FCPS High School chromebooks (`drawper`) have NOT been tested with shimboot yet.

Full writeup is available here: https://github.com/catfoolyou/Block-Bypass/blob/main/shimboot.md

## Br1ck
It is capable of unenrolling all devices with a Cr50 chip on the latest version, v130. It has a low chance of being patched without a release of a new Chromebook model.

Theoretically it should work on all FCPS chromebooks, and some people have actually used it successfully.

`nissa` chromebooks (the G11 ones) will PROBABLY not work. Don't come back here bitching about it.

Full writeup and instructions are here: https://br1ck.vercel.app/

## CRSH2TTY - Universal unenrollment (PATCHED)
*I think this might have been patched...*

CRSH2TTY is a universal unenrollment method created by @TN Partnered and @TN Partnered 2 

How do I do it?
1) Powerwash (ctrl + alt + shift + r on the login screen)
2) Proceed through setup as normal
3) When it starts to enroll wait 1-2 seconds (no longer) and perform an EC reset (refresh + power)
4) When it starts to enroll again wait 1-2 seconds (no longer) and enter recovery (esc + refresh + power)
5) Leave if off for at least 15 hours (or longer, I would just leave it overnight)
6) When you turn it on you should be unenrolled!

Writeup: https://github.com/kuromuiroha/crsh2tty

## OLYBmmer/BadRecovery
BadRecovery unenrolls ALL devices that are EOL before 2024, and can unenroll current supported devices on kernel version 3 or lower.

Instructions are available here: (I am too lazy to make a proper writeup)

https://github.com/BinBashBanana/badrecovery

## Skiovox exploit
This was patched I think

https://github.com/3kh0/ext-remover/discussions/929

## Webview exploit
A random hole in chrome login that allows for unrestriced browsing (one tab only)

1) Add an account to chrome or go to chrome://chrome-signin on a chromebook
2) Enter `google@d11.org` as the email and complete the captcha/security check
3) Click sign-in options
4) When prompted, click Sign in with Github
5) Click on Docs
6) Scroll to the bottom and click on Pricing
7) In the search bar type "google"
8) In the right sidebar click on `google.com`
9) You now have a tab that is unaffected by any extensions

## Chromebook specs
FCPS chromebook specs:
https://cros.tech/device/drawper/

HP specs sheet: https://h20195.www2.hp.com/v2/GetDocument.aspx?docname=c07811220

HP specs on website https://support.hp.com/us-en/document/ish_5492565-5492609-16

FCPS chromebook board and shims (recovery images):
https://chrome100.dev/board/dedede

# BYOD shits and bypasses

## Wifi instructions
Based on the recent changes pushed by FCPS, the best way to bypass their restrictions is to BYOD. 

**You can also do this if you unenrolled your chromebook or flashed a Windows laptop (if you have one somehow)**

To properly do BYOD, you *probably* shouldn't use the FCPS provided installer as your go-to option. Instead, use the wifi passwords in this repo to connect to their wifi directly (if that works).
The certs that I managed to get my hands on may or may not work. Afaik it depends on the computer and/or the OS.

To use the installer, sign in a GUEST, NOT with your FCPS username. Download the certs manually and install as per the instructions provided. DO NOT use `2.2.2.2`, use `https://xprsscnctvm.fcps.edu/enroll/FairfaxCountyPublicSchools/Production/reset` instead.

## Chrome DNS (BYOD only)

If you are bringing your own computer, you can do this to prevent sites being blocked

[Explanation for dumbasses like me](https://simpledns.plus/kb/195-how-to-enable-dns-over-https-doh-in-chrome)


![image](https://github.com/user-attachments/assets/9bcbfb46-ba32-4f2e-a4c4-6a0c6bf86684)

# Browser games and other crap
Again, use a [proxy](https://github.com/catfoolyou/Ultraviolet-App) to access blocked websites. Be advised that games (and sometimes yt) are somewhat laggy over a proxy connection.

If [catfoolyou.github.io](https://catfoolyou.github.io) is blocked, a mirror of my website is available [here](https://eldritchdev2.github.io/Website-v2/)

### Eaglercraft and FNAW:
The latest 1.5.2 and 1.8.8 offline clients are available for download, as well as Five Nights at Winston's.

### Other games:
Doom, Retal, Quake, Slope, Bananabread and all of the other games that must run in a web environment cannot be run locally. Might migrate my site soon.
