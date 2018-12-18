---
title: Supported features
tags:
  - getting_started
keywords: "features, capabilities, comparison, benefits"
last_updated: "December 17, 2018"
summary: "Collection of features available in DeltaWave"
published: true
sidebar: mydoc_sidebar
permalink: mydoc_supported_features.html
folder: mydoc
---


## Supported features

Features      | Notes
--------------|-----------
Reads WAV, FLAC, DSD files | Supports 16, 24, 32 bit WAV and FLAC files, as well as various DSF files with DSD64, DSD128, and DSD256 format
Level differences | Accurately computes and corrects for level differences between files
Phase correction | Determines and corrects for fractional phase offset down to 1/1000 of a sample
Clock Drift correction | Determines and corrects for clock drift between two files
Low/High pass filtering | Can filter both files to allow only lower or higher frequencies into the final comparison
Notch Filter | Allows the use of a single notch filter to remove a specific frequency component. Useful when testing or comparing simple sinewaves
Skip samples | Skip any number of samples at the beginning and the end of each file
Control all Settings | Detailed settings can be configured for each of the processing units in DeltaWave. Settings can be saved to become default.





## Features not available yet in this version


Features |  Notes
--------|-----------
Process files larger than available memory | Planned for future release
Faster load time for DSF format files | Planned for future release
Audio Playback | needs work -- currently some parts are broken

{% include links.html %}
