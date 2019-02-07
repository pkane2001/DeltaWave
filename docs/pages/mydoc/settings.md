---
title: Settings
tags: [settings]
keywords: settings, configuration, customization, fft, gain, enable, disable
last_updated: December 17, 2018
summary: "Version 1.0.1b of DeltaWave is the initial beta release of this software. Use at your own risk!"
sidebar: mydoc_sidebar
permalink: settings.html
folder: mydoc
comments: true
---

## Configuration Settings (Setup)

Configuration settings are available by clicking the gear icon at the top right of DeltaWave window.

![waveform](images/img6.png)

* Any changes you make to the settings are automatically updated when you close the Setup window
* Settings are automatically saved and reloaded the next time you start DeltaWave
* You can optionally save current settings in a separate file by selecting File menu on DeltaWave main window and chosing Save Settings
* Setting changes are applied the next time you click on Match or Show button

### General Settings

Setting  | Description
-------- | -----------
Resample UP to the same rate | When two selected files are not sampled at the same frequency, this option tells DeltaWave to upsample the lower rate file to the higher rate one. By default, the opposite is true: the higher rate file is downsampled to the lower rate one.
Correct Phase Drift | If clock drift is detected during processing, this tells DeltaWave to attempt to adjust this out. This allows two files recoreded with slightly differing clocks to be properly matched up. On is the default setting.
Match Gain | Compute and adjust the levels of the two files, if different. On is the default setting.
Prompt to invert phase | If two files are detected to be inverted relative to each other, this will prompt you to confirm if you want to correct this. The default is off, meaning DeltaWave will just correct the phase without asking you.
Dither to original bit size | When selected, the processed files (normally handled in double-floating point format) will be dithered to the original bit size, ensuring the same precision of samples as in the original files.
Offset Precision | This determines the precision of the partial sample offset calculation, in decimal places. Default of 8 means the calculation stops when there is no more improvement up to 8 decimal places. More precision will take longer for the calculation to converge, usually without a major improvement in match quality. 

### Spectrogram Settings

Setting  | Description
-------- | -----------
FFT Size | Larger size increases frequency resolution, but slows down processing. Very large size can result in a very slow display of the spectrogram plot
Window   | Different windows will have slightly different effect on FFT processing
Steps    | Number of time steps (horizontal axis) to display. Larger number will result in greater time resolution, but also in many more FFT calculations, slowing down processing and the spectrogram plot


### Resampling Settings

Setting  | Description
-------- | -----------
FFT Size | Not used
Window   | Different windows will have slightly different effect on resampling processing


### Spectrum Settings

Setting  | Description
-------- | -----------
FFT Size | Larger size increases frequency resolution, but slows down processing 
Window   | Different windows will have slightly different effect on FFT processing
Peak Hold |  Instead of averaging each FFT window, the plot will show maximum (peak-hold) value for that frequency bin

### Cepstrum Settings

Setting  | Description
-------- | -----------
FFT Size | Larger size increases frequency resolution, but slows down processing 
Window   | Different windows will have slightly different effect on FFT processing

### Low Pass Filter

Setting  | Description
-------- | -----------
FFT Size | Not used 
Window   | Different windows will have slightly different effect on FFT processing

___
{% include links.html %}
