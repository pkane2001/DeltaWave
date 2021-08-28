---
title: Impulse Response
tags: [IR]
keywords: IR,Impulse Response
last_updated: April 20, 2021
summary: "Version 2.0 of DeltaWave. Use at your own risk!"
sidebar: mydoc_sidebar
permalink: ir.html
folder: mydoc
comments: true
---

## What's new?
DeltaWave now has the ability to compute a precise Impulse Response of a device by doing what it does best: computing a null difference between two files. The reason IR is important is that it characterizes the time-linear behavior of the device. IR contains enough information about the device to compute the frequency and phase response of the device. As an example, this can be used to analyze the filter response of a DAC/ADC loopback recording.

What's more, IR can then be used to construct a correction to remove frequency and phase errors from the    device signal, or to apply the same errors to a digital file to simulate the effect of the device!

![Impulse Response 1](images/ir1.png)


## Short list of capabilities starting with v1.0.65:

* Compute and record IR representing the differences introduced by the measured device from the difference between digital source file (reference) and the recording through the device (comparison). As always, the recording can be a piece of music or a generated signal
* Average multiple recordings to produce a higher quality IR. This reduces noise and improves IR accuracy
* Automatically run the IR generation and averaging for multiple files, in one step
* Save and load generated IR averages
* Apply saved IR averages to undo the errors introduced in the comparison file or future recordings with the same device
* Display IR on a plot for analysis and comparison
* Export the inverse IR as a 32-bit floating point WAV file that can be used by convolution engines for play-back and measurements

## Impulse Response

Impulse response of an audio device is normally the output of that device when a single, instantaneous pulse is presented at the input. The output is then recorded and analyzed to produce a usable IR representation that can be measured and corrected. Other software use frequency sweeps, chirps, etc.

With DeltaWave, the process is similar, but instead of an instantaneous pulse, DW uses a recording of music (or other signals) to derive IR. The benefit is that IR can be computed with greater accuracy and greater SNR (signal to noise ratio).

![Impulse Response 2](images/ir3.png)

## Usage

There are a few main functions available when using IR within DeltaWave:

1. Turn on recording to average one or more IRs
2. Run one or more pairs of files through the Matching process to record IR
3. Optionally save resulting IR
4. Optionally view resulting IR on a plot (Impulse Response tab)
5. Turn on IR correction in DeltaWave
6. Run one or more Match comparisons: the inverse of the recorded IR will be automatically applied during the match to correct for known device deficiencies
7. Export inverse IR to a WAV file for use with Convolution engines for playback or measurements

## IR Indicator and menus
All of IR functions can be accessed from the IR indicator located between the Delta waveform entry box and the volume control:

![Impulse Control](images/IRControl.png)

IR Indicator control has three states:

"+" when it's recording new IR and averaging these
"IR" when no IR is recorded
"✓" when IR has been recorded and the inverse will now be applied to future Match operations

You can switch between these three states simply by clicking on the IR indicator.

The number to the top right of the IR indicator shows how many averaged IRs have been collected so far. 0 means none.

In addition, you can right click on the IR indicator to display the Process->IR menu with the following options:

![Impulse Response Menu](images/ir2.png)

* Record Average IR (x) -- selecting this will start the IR recording process. All subsequent Match operations that produce non-linear EQ will also add to the averaged IR, automatically
* Correct Using Average IR -- selecting this will tell DeltaWave to apply IR corrections to future Match operations. Recording of IR will be automatically turned off, but can be re-enabled later
* Clear IR Averages -- will erase all collected IR data in memory, the number of IR averages will be reset to 0. Saved IRs will not be touched.
* Load... -- load a saved IR correction 
* Save... -- save current in-memory IR with one or more averages
* Export IR as WAV... -- save current in-memory IR to a 32-bit floating point WAV file (mono) to be used in a convolver or imported into REW or similar software
* Average Multiple... -- allows multiple files to be selected to build a large average IR. Each file will be loaded, a Match operation will be performed, and the resulting IR will be added to the average. All of these will be processed automatically. When done, you can save the resulting IR, export it, or apply as a correction:
 
![Impulse Response 1](images/IRCruncher.png)


All feedback and suggestions are welcome!
