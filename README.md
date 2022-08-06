# intech-en16-ableton

An effort to make Intech EN16 Controller work as expected in Ableton 11.


This repository contains presets and profiles for Grid Editor by Intech, as well as User Remote Script mappings for Ableton.



## Usage

1. Copy presets and profiles from `intech-en16-ableton` to your Grid Editor's directory with presets and profiles
2. Set one of the profiles to use with all pages (or just the first one) your EN16 in Grid editor and save it. The only thing that profile does on top of the default one is setting all encoders to Binary Offset Relative Mode so it will work properly with Ableton
3. Copy directories from `Ableton User Remote Scripts` directory to appropriate place for User Remote Scripts for your platform (usually `/Users/[Username]/Library/Preferences/Ableton/Live x.x.x/User Remote Scripts.` on Mac and `:\Users\[Username]\AppData\Roaming\Ableton\Live x.x.x\Preferences\User Remote Scripts` on Windows) - most relevant directories are listed in [Ableton Docs](https://help.ableton.com/hc/en-us/articles/206240184-Creating-your-own-Control-Surface-script)
4. Launch Ableton, open MIDI settings, select a control surface and select your Grid device for MIDI input and output.

This should be enough to get everything to work.


## Available Control Surfaces

The mappings feature the following layouts:

1. `Intech Grid EN16` - bottom 8 encoders on the first page of the device automap to macro knobs of currently selected device in Ableton
2. `Intech Grid EN16 with mixer` - same as `Intech Grid EN16`, and on top of that bottom 8 encoders of the first page are mapped to volume sliders of the first 8 mixer tracks.


## General Recommendations

1. Whenever you map an encoder manually in Ableton, don't forget to select RelativeBinOffset mode (you can page through modes by rotating the encoder while mapping, no need to manually click the dropdown menu)
2. If you're not happy with the mappings, you can always change them in `UserConfiguration.txt` file. Note, that MIDI CC channels are zero-based in this file, so value `0` represents channel `1` (as viewed in Ableton UI)


## Making LEDs on EN16 follow actual values in Ableton

I've never tried it, because I don't really find this useful, but if you're interesting in implementing it, you can try following this guide from Intech: https://intech.studio/feed/receive-midi-from-ableton-with-grid-controllers

If you succeed, please consider making a pull-request to this repository.

# Have fun!
