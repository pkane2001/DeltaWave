---
title: Release notes
tags: [getting_started]
keywords: release notes, announcements, what's new, new features
last_updated: August 16, 2021
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

## Changes in 1.0.71b
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

## Changes in 1.0.64b
* Change: Added a *View->Chart Options->Linearity index to 0* menu option to turn on/off linearity plot normalization (on by default)
* Added: FFT Scrubber processing and plot window with audio scrubbing
* Added: two new, smaller Spectrogram FFT Size settings: 256 and 512

## Changes in 1.0.63b
* Fix: Settings window toolbar can overlap text below under certain DPI settings
* Fix: Exception and stop processing when linearity plot contains too few samples in the lower few bits
* Fix: When subsample correction is enabled but drift correction is turned off, small delays below 1/1000000 of a sample might still be processed and applied, unnecessarily. These were properly ignored if drift correction was enabled

## Changes in 1.0.62b
* Added: Configuration selection in Setup window, along with reset and save options
* Added: Command-line arguments to automatically process files and write out the result
* Added: Set Trim levels to current Zoom level menu under Edit
* Added: Play zoomed-in portion of wave file menu under Play
* Added: PK Metric column and optimization option to Manual Adjustments window
* Added: Option to display and enter gain settings in DB in Manual Adjustments window
* Added: Right click pop-up menu for showing/hiding tabs (right-click on any visible tab)
* Added: Linearity measurement at 0.5dB error (in bits)
* Added: Check/uncheck button to select or unselect all tabs in the Setup window
* Changed: Manual Adjustments window will now apply new file trim settings, if changed
* Changed: Frequency axis log scale labels should work better with high-resolution displays, previously could cause overlaps
* Changed: sub-sample offset calculation to work better with noise signals
* Changed: zero value in "Take" trim level will now result in taking the whole file, just like it does with "End" setting. Previously resulted in error message


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
 

___
{% include links.html %}
