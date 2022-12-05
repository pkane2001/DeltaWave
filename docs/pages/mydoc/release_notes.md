---
title: Release notes
tags: [getting_started]
keywords: release notes, announcements, what's new, new features
last_updated: July 19, 2022
summary: "Version 2.0 is free software. Use at your own risk!"
sidebar: mydoc_sidebar
permalink: release_notes.html
folder: mydoc
comments: true
---

## What is it?
DeltaWave is an experimental software built to allow detailed comparison of two different captures of the same audio signal.
It was inspired by the idea of [Audio DiffMaker](http://www.libinst.com/Audio%20DiffMaker.htm), but it is a completely new piece of software, written from scratch. No parts of Audio DiffMaker were used in DeltaWave. Calculations and algorithms used in DeltaWave are also different, and results are more than likely not agree between these two programs. As I was never successful at using *Audio DiffMaker* but wanted to, DeltaWave was born.

## Is it free?
DeltaWave is provided to you free of charge, and contains no advertisements or in-program purchases.

## What can I do with it?
As the most basic function, DeltaWave allows an objective measure of how different two captures of the same audio signal might be.

Examples where this can be useful include:

* Compare analog and digital captures of the same track
* Compare two different digital formats of the same track (different number of bits, different sampling frequency, different filtering, or even difference between PCM and DSD formatted files)
* Determine how much of a difference an electronic component makes on the output of an audio system
  * Audio interconnects
  * Power cables
  * Digital/USB interconnects
  * Pre-amps
  * DACs
  * Amplifiers
  * etc.
*  Visualize audio waveforms using:
   *  Zoomable wave comparison plots
   *  FFT Spectrum analysis charts
   *  Cepstrum analysis
   *  Spectrograms
   *  Phase differences
* Listen to each track, individually
* Listen to the difference track after subtracting the two
* Write out the difference track as 32-bit or 64-bit WAV file for external analysis


## Changes in 2.0.8 - [link to discussion](https://www.audiosciencereview.com/forum/index.php?threads/beta-test-deltawave-null-comparison-software.6633/post-1400890)
* Fixed: Loopback recorder using different ASIO drivers for input/output
* Fixed: Recorder not restoring settings when re-invoked
* Fixed: Error after first installation saying settings file was not found
* Fixed: One empty channel recorded in 'stereo' mode with ASIO
* Fixed: Recorder can now be launched with or without reference/comparison files specified in the main window
* Fixed: Error "Invalid number of input channels 2" when using ASIO output device
* Fixed: recorder always plays both cannels, even if only one channel is selected
* Changed: removed option to launch DeltaWave from the installer -- was causing errors due to some installation tasks still being incomplete

## Changes in 2.0.4 - [link to discussion](https://www.audiosciencereview.com/forum/index.php?threads/beta-test-deltawave-null-comparison-software.6633/post-1253063)
* Added: Loopback recorder - play, record, and measure all in one click!

## Changes in 2.0.3
* Added: WASAPI Exclusive/Shared setting
* Added: % match to the output of the batch-file mode (command line execution)

## Changes in 2.0.2
* Added: support for reading WAVEX (extended WAVE format) files

## Changes in 2.0.1
* Fix: regression issue with color scaling of delta spectrograms
* Changed: IIR filter replaced with the maximally flat in-band Butterworth version
* Fix: FIR filter could previously cause a small error near DC frequency
* Added: additional filter sizes (8M and 16M taps)


## Changes in 2.0.0 - [link to discussion](https://www.audiosciencereview.com/forum/index.php?threads/beta-test-deltawave-null-comparison-software.6633/post-893612)
* This is the first official release without the "beta" designation (!)
* Added: fully functional version of the log-frequency spectrogram
* Changed: improved speed of update on spectrogram plots
* Added: additional menu options to hide/show multiple tabs on right click on a tab
* Improved:  accuracy of the Sinc resampler
* Improved:  accuracy of the subsample offset determination
* Improved: made charts update quicker during a match operation
* Fix: minor clean up to additional edge condition handling
* Added: new resampler rates,  352.8k, 384k, 705.6k and 768k
* Added: the full list of FFT Windows to all drop-downs on the Setup screen

## Changes in 1.0.71b - [link to discussion](https://www.audiosciencereview.com/forum/index.php?threads/beta-test-deltawave-null-comparison-software.6633/post-881489)
* Added: option to show samples and sinc-interpolation on extremem zoom-in of waveform
* Added: non-linear EQ option to correct for small linearity errors
* Changed: log frequency display is now using more logical steps, showing easier to read frequencies instead of fractions
* Fixed: a number of edge conditions that could result in the match operation terminating prematurely
* Reverted: removed log-frequency display in spectrograms due to incorrect labeling at certain sampling frequencies. I'll try to fix it in the future.


## Changes in 1.0.70b
* Added: support for log-frequency display in spectrograms
* Fixed: the name of FFT window Tukey0.01 was misspelled
  

## Changes in 1.0.69b
* Added: minimum phase filters can now be used in addition to linear phase ones
* Changed: Improved group delay plot to more closely match phase variations
* Changed: Cepstrum plot to use time (quefrency) scale on the X-axis, changed annotations to show frequency and time

## Changes in 1.0.68b
* Fixed: 64-bit WAV files header changed to WAVE_FORMAT_IEEE_FLOAT from WAVE_FORMAT_PCM
* Added: Support for loading 8-bit unsigned WAV file format

## Changes in 1.0.67b
* Fixed: upsampling caused an index out of range error under certain conditions
* Added: FFT Scrub plot will now update automatically in sync with playing music
* Added: A few new sizes of Tukey FFT Windows
* Added: Import of IR WAV-format files


## Changes in 1.0.66b
* Fixed: matching of files smaller than FFT Size (caused an error previously)
* Changed: units labeled "V" changed "Amplitude" in IR plot viewer to better reflect value from -1 to 1
* Changed: IR plots are now interpolated
* Fixed: Plot refresh button now refreshes IR plot

## Changes in 1.0.65b
* Added: Impulse Response averaging, correction, and export
* Added: Impulse Response plot with selectable units
* Added: Frequency response file exports in REW text format
* Changed: Reorganized File menu
* Added: In FFT Scrub control, hold down Control key while using mouse wheel to accelerate scrubbing by 50x
* Changed: selected zoom levels per chart are now saved with the settings and will be in effect next time DeltaWave is started
* Changed: added option to save/reload custom zoom settings for all plot windows
* Changed: Small adjustment in gain difference computation for improved accuracy
* Added: FFT Scrubber now displays RMS values of the three signals (Ref, Comp, Delta)

___
{% include links.html %}
