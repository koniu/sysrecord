# sysrecord

A simple script for recording system sound with ALSA, JACK or PulseAudio.


## Description

`sysrecord` is a simple script for one-click recording of system sound.
It's designed to be hooked up to a dedicated button (such as the blue
button on thinkpads or a remote control) and used for easy recording of
samples from any source. It detects whether a sound daemon (such as JACK
or PulseAudio) is running and uses appropriate utilities to record whatever
is playing through the speakers.


## Usage

1. Make sure your audio subsystem is configured correctly (see *Requirements*)
2. (optional) Put `sysrecord` in your executable PATH (eg. `/usr/local/bin`)
3. Run `sysrecord` to start recording
4. Run `sysrecord` again to stop recording


## Requirements

### General

* `bash` or `zsh`
* properly configured audio subsystem (see *Requirements* below, PulseAudio should work
  out of the box).
* (optional) `osd_cat` - from `xosd-bin` package, for visual feedback during recording
* (optional) `notify-send` - from `libnotify-bin` package, for displaying notifications
* (optional) `soxi` - from `sox` package, for reporting duration of the recording

### PulseAudio

* `pulseaudio` daemon running
* `parecord` (`pulseaudio-utils` package)

### JACK

* `JACK2`
* `jackdbus` running
* `jack-capture`

### ALSA

* `snd-aloop` module loaded
* `~/.asoundrc` like the example in this repository
* `arecord` (`alsa-utils` package)



## Contact

* [GitHub repository](https://github.com/koniu/sysrecord)
* Author < koniu at riseup dot net >


