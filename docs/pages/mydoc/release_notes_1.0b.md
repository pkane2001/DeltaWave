---
title: Release notes
tags: [getting_started]
keywords: release notes, announcements, what's new, new features
last_updated: February 7, 2019
summary: "Version 1.0.5b of DeltaWave is the initial beta release of this software. Use at your own risk!"
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

This is an early beta version of the software and is set to expire in 60 days. Please check this website before then to get an updated copy!

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
* Write out the difference track as 32-bit WAV file for external analysis

## What is new in version 1.0.5b?

* Added logging for problem reporting and troubleshooting. Available under Help->Logging Menu
* Added A-Weighted measurements to better represent audible differences, shown as dBA value in RMS Difference and Correlated-Null values. This applies greater weight to frequencies that the human ear is sensitive to.
* Fixed linear drift correction. Should work much better than in the previous version (turn off NonLinear Drift correction setting)
* Improved clock drift calculation, works more consistently and accurately
* Added tab display selection in settings. You can now chose what tabs and charts will be available after a Match. This also controls what plots will be included in a report: any plot that is not visible will not be included.
* Added a Plot showing Delta of Spectra -- this is the spectrum of Comparison file subtracted from the spectrum of Reference. The closer this is to a flat line at zero, the better the spectra match between two files.
* Improved, formatted display of the results on the status bar
* File menu now has two additional options 
  * Save Compare File
  * Save Delta File
* 


___
{% include links.html %}