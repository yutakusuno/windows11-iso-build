## Description

[UUP Dump](https://uupdump.net) is a tool that allows you to create a custom Windows 11 ISO file from any public preview.
This makes it possible for us to use Window11 on Mac with such as VMware Fusion. And more, you can use it for free within individual use.

Here is a summary of the way of creating an ISO image file on an Apple Silicon Mac(M1/M2).

## Getting Started

### Download the UUP file

First, please download a UUP file on [UUP Dump](https://uupdump.net).
If you don't have a specific preference, select `Latest Public Release build` and press the arm64 button.

### Set environment

These are required to build an ISO image file.

```
brew tap sidneys/homebrew
brew tap minacle/chntpw
brew install aria2 cabextract wimlib cdrtools minacle/chntpw/chntpw
```

If you get an error when installing chntpw, this issue may be helpful.
https://github.com/sidneys/homebrew-homebrew/issues/2

### Create the ISO image file

`uup_download_macos.sh` is the bash script to create the ISO image file on Mac.
 It takes about ten minutes to complete.
 
```
cd 22621 # This directory was installed at the procedure of `Download the UUP file`.
bash uup_download_macos.sh
```

Upon completion, the ISO image file will be created such as `22621.1_MULTI_ARM64_EN-US.ISO`.
