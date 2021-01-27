---
title: Release notes
tags: [getting_started]
keywords: release notes, announcements, what's new, new features
last_updated: Dec 24, 2020
summary: "Version 1.0 of DeltaWave is the initial beta release of this software. Use at your own risk!"
sidebar: mydoc_sidebar
permalink: release_notes_1.0b.html
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


## Changes in 1.0.57b
* Added: ERB trend-line option for FFT plots in settings
* Added: [PK Error Metric and screen](pk_metric.htm)
* Changed: phase unwrap behavior and algorithm
* Added: ERB trend-line as Group Delay added to uncorrected Delta Phase plot

## Changes in 1.0.56b
* Fix: Drift correction could result in a decrease in higher frequencies in the spectrum plot
* Fix: Turning off drift correction would not clear the previously computed data in the Clock Drift plot


## Changes in 1.0.55b
* Fix: Delta spectrogram dB range set incorrectly to the same as Spectrogram 1 & 2

## Changes in 1.0.54b
* Added: new FFT window types, including multiple Kaiser
* Added: FFT Window explorer with time- and frequency-domain plots and measurements
* Changed: Delta Spectrogram window scale is now locked to Spectrogram 1 and 2
* Fixed: Under one specific combination of filter settings, filter 1 @start was being ignored

## Changes in 1.0.53b
* Added: support to process .mp4, .m4a, and .alac files
* Added: 2M FFT size for non-linear EQ settings
* Added: Some new Cosine and Flattop FFT windows
* Fixed: When using manual adjustment window Gain setting was ignored and recalculated each time
* Changed: Group delay computation changed to reduce time and memory needed to process
* Added: Double-clicking on the trim label "End" or "Take" will switch between these two modes

## Changes in 1.0.52b
* Fix: error on some computers with no permission to query memory statistics
* Fix: filter 1 settings for LP and HP filters @ start were not being processed
* Fix: measure simple waveforms option interrupted alignment process

## Changes in 1.0.51b
* Change to automatically pick a better size for cross-correlation depending on data
* Change to reduce iterations when computing drift
* Added option to change the file trim end setting from how many to trim to how many to include
* Added larger size FIR filter setting, up to 1M taps
* Fixed bug that could result in a few zero samples being added at the very end of comparison file
* Modified memory management to improve handling of files larger than a couple of minutes

## Changes in 1.0.50b
* Changed linearity computation to improve consistency and reduce the random jumps in the plot


## Changes in 1.0.49b
* Added DF metric for measuring differences between waveforms [Reference AES PDF](http://soundexpert.org/documents/10179/11017/DiffLevel_AES118.pdf)
  
## Changes in 1.0.48b
* Fixed some samples set to at the end of of a FLAC file by Naudio.FLAC reader
* Changed drift computation for simple waveforms to produce a more predictable result

## Changes in 1.0.47b
* Put back group delay plot removed in v.46
* Added separate FFT Window option to non-linear EQ (previously used the same window as Spectrum settings)
* Improved jitter error result with simple waveform measurements
* Fixed the amplitude increasing by x4 when using simple waveform measurements combined with drift correction


## Changes in 1.0.46b
* Added non-linearity plot
* Added legend and harmonic arrows option to matched spectrum plot
* Clock Drift correction now works in simple waveform measurement mode
* Fixed Kaiser window not producing correct results when FFT size is equal to the number of samples
* Turned off curve fitting in phase plot (made the plot too busy and often looked chaotic)
* Improved the quality of up/down sampling, added appropriate level of dither for the original bit size
* Changed lower limit on plots to -400dB from -300dB

## Changes in 1.0.45b
* Added option to align and compare simple periodic waveforms
* Added THD, THD+N, and Dynamic Range calculation when measuring simple sine wave
* Added overlay options to time-domain waveform plots

## Changes in 1.0.44b
* Fix for index out of bounds when downsampling 48k to 44.1k files

## Changes in 1.0.43b
* Fix for phase and spectrum plots having very small differences between runs
* Fix for volume going down after a second of play from the main window

## Changes in 1.0.42b
* Fix Non-linear EQ not working
* Fix artifacts displayed at the very end of a spectrogram
* Add color palette selection for Spectrograms with many to choose from
* Add the ability to overlay spectrum plots from previous match runs, including those loaded from disk


## Changes in 1.0.40b
Fixing a few regression items from .39:
* Re-enable dynamic volume adjustment while playing form the main window
* Fix wrong color used in Spectrogram when all values are the same (e.g., 0dB)
* Fix "Stopped! Matrix dimensions must agree: op1 is ..., op2 is ..." error

  

___
{% include links.html %}
