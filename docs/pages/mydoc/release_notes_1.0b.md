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

## Changes in 1.0.61b
* Fixed: auto-trim function under some conditions could result in extra zero samples being added to the waveform


## Changes in 1.0.60b
* Fixed: regression in 1.0.59 could cause an index out of bounds error when processing "stereo" channels with inverted absolute phase


## Changes in 1.0.59b
* Fixed: corrected sub-sample matching behavior of simple/periodic waveforms (regression from .58)
* Added: Automatic trim of silence at both ends of a file when using Auto-Trim option
* Added: Automatic detection of simple/periodic waveforms. If simple waveforms option is not on, user will be asked to turn it on
* Changed: Improved THD+N measurements for simple (single frequency) waveforms
* Fixed: dB display in THD frequency plot for simple waveforms -- used to display in scientific notation the first time it's used

## Changes in 1.0.58b
* Added: Separate setting for sub-sample alignment, independent of drift correction
* Added: Additional values for phase and non-linear threshold settings
* Changed: setting changes are saved immediately when exiting settings window, not when exiting DeltaWave as before
* Fixed: group-delay/phase trend plot should be a better curve fit to the phase plot
* Fixed: phase limit setting now works as expected, was ignored previously
* Added: (experimental) 400ms window filtered error signal in PK Metric plot. Hold down Ctrl key while mousing over the main plot to update.
* Fixed: File end trim/take settings are now enforced up to the sample. Previously could vary based on file buffer size.


## Changes in 1.0.57b
* Added: ERB trend-line option for FFT plots in settings
* Added: [PK Error Metric and screen](pk_metric.html)
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

 

___
{% include links.html %}
