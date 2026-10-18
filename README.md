<div align="center">

# Punch Cut

**Zooms and transitions on talking-head video, without keyframes.**
Free to download. Windows 10 and 11, 64-bit.

[**Download the latest Punch Cut**](https://github.com/ByronLangley/punch-cut/releases/latest)

</div>

## What it does

You scrub to a moment, press one key, and the picture punches in. Or Punch Cut reads your footage, finds the Cuts already in it, and places the zooms for you. Then it exports a finished MP4.

- **Zoom in and Zoom out** at any moment, with no keyframes.
- **Find my cuts** reads your footage for jump cuts and changes of shot.
- **Face framing** aims each zoom at the speaker's face.
- **Transitions at a Join**: Whip, Swap and Zoom through, or No transition.
- **Export** gives you a finished MP4, and the preview you watch matches it frame for frame.

Everything runs on your own computer. Punch Cut sends nothing anywhere unless you press Send in its Send window.

## Install it

1. Open the [latest release](https://github.com/ByronLangley/punch-cut/releases/latest) and download **Punch-Cut-Setup-0.1.1.exe** (about 230 MB).
2. Double-click it. It installs for your own Windows account only: no administrator password, nothing to choose.
3. Open Punch Cut from the Start menu or the shortcut on your desktop.

Punch Cut brings everything it needs. You don't have to install Python, FFmpeg or anything else first.

## Windows will warn you first

The first time you run the installer, Windows shows a blue box that says **"Windows protected your PC"**. Your browser may also say the file "isn't commonly downloaded" before that. Neither means something is wrong.

**Why it appears:** Windows warns about any program that hasn't been signed by a company Microsoft has verified, and about any new program that few people have downloaded yet. Signing costs a yearly fee and waits until enough people use the app. Punch Cut's installer isn't signed yet.

**How to get past it:**

1. In the blue box, click **More info**. (The box shows only a **Don't run** button until you do.)
2. Click **Run anyway**.

If your browser stops the download first, open its downloads list and choose **Keep** (in Edge, **Keep** and then **Show more** and **Keep anyway**).

**To check you have the file I published:** every release lists its installer's SHA-256 fingerprint in the release notes. In PowerShell, `Get-FileHash .\Punch-Cut-Setup-0.1.1.exe` should print the same value.

## Sending a message or a problem

In Punch Cut, open **Help → Send a message…**, write what you want to say, and press **Send**. The window shows you exactly what will be sent before you press it, and nothing goes unless you do. If Punch Cut crashes, it offers to send a crash report the same way, and asks you every time.

A crash report carries the Punch Cut and Windows versions and the errors Punch Cut recorded. It never carries your footage, and it never names your Windows user folder.

## Uninstalling

Use **Settings → Apps → Installed apps → Punch Cut → Uninstall**. It asks "Also remove my saved sessions and settings?" and starts on **No**, which keeps them so Punch Cut opens on them if you install it again.

## The code, and the parts Punch Cut includes

Punch Cut itself is free to download and use. Its code is not published here: this page holds only the installer, the release notes and this page.

Punch Cut includes other people's software, each under its own licence, which you can read inside the app at **Help → About Punch Cut and licences**. One of them is **FFmpeg**, which the installer carries as a program built with libraries under the **GNU General Public License, version 3** (and the licences of those libraries). The licence entitles you to the source code of that program, so the source is offered right here, next to the installer, in every release:

- **`ffmpeg-2a571b6068-source.tar.gz`**: FFmpeg's own source code, at the exact commit the program names (`2a571b606854520cf89804d8030c8b328e621689`: FFmpeg 9.0.2 and the 17 changes made after it on FFmpeg's 9.0 branch).
- **`ffmpeg-builds-6c9aec5fc9-source.tar.gz`**: the scripts that built that program, with their patches, at the exact commit that built it (`6c9aec5fc9a72ec3abedd1fa84db141fa18cf52b`).
- **`ffmpeg-libraries-source.zip`**: the source code of every library compiled into that program (x264, x265, libvpx, libaom, Opus, LAME and the rest), each at the version the build scripts pin, one folder per build script.
- **`FFMPEG-SOURCES.md`**: the list that goes with them. For every library it gives the licence, the version, the SHA-256 of its source file and where it came from upstream, and it says what is left out and why.

Punch Cut's FFmpeg is the GPL build [BtbN](https://github.com/BtbN/FFmpeg-Builds) made on 30 September 2026, unchanged. BtbN's build scripts are public, and the copy here is the one that built it. Punch Cut 0.1.0 carried gyan.dev's 9.0.2 "essentials" build instead, and the 0.1.0 release still offers that build's source. If you want any of it on a disc, [open an issue on this page](https://github.com/ByronLangley/punch-cut/issues) asking for the FFmpeg source and I will get it to you. This offer lasts at least three years from the date of each release.

## About the name

Punch Cut was called Zoom Studio until October 2026. "Zoom" is another company's trademark, which is why it was renamed.
