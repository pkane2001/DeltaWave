---
title: DeltaWave Comparator
tags: [ABX, compare, comparator]
keywords: ABX, compare, comparator
last_updated: February 26, 2019
summary: "Version 1.0b of DeltaWave is the initial beta release of this software. Use at your own risk!"
sidebar: mydoc_sidebar
permalink: comparator.html
folder: mydoc
toc: true
datatable: true
comments: true
---

After creating that near-perfect match using DeltaWave, wouldn't it be nice to be able to compare the two files that are perfectly aligned in phase and level? Enter the Comparator. Comparator is a tool that allows you to run both, sighted, and blind audibility tests to determine if the two files have sufficient differences to be detected in playback. 

<img src="images/img10.png" style="vertical-align: middle" />

## Where is it?

Comparator is available from the Play menu on the main DeltaWave window. Two files must be loaded, and optionally aligned before invoking it. The two files can be loaded by pressing either Show or Match buttons.

## Play Controls

The main controls for ABX or AB-style comparison are the large buttons, A, B, and X. These buttons control which waveform is played back through the audio device selected on the main DeltaWave window.

* A will play the reference file
* B will play the comparison file
* X will play a randomly chosen A or B file

These buttons do not require a mouse click, simply moving a mouse over the large square will play the selected file. This allows a quick switch between two of them by simply moving the mouse back and forth.

The slider controls on the bottom allow you to select a portion of the track to focus on. This portion will be used for all comparisons and will be repeated as long as any of the play buttons are selected. The chart above is the Delta Waveform chart of the two files. This can give you an idea of where there are larger (level) differences between the two files, so you can try to narrow your selection to those areas, as there are likely to be more audible differences.

## Volume

Volume control is the vertical slider on the right. This controls the playback volume of both files. No volume adjustment is applied when this is set to 0dB.

## AB Comparison
A simple, non-blind A/B comparison is easy to do using the Comparator. Simply chose a section of the tracks (or the whole track) that you want to compare, set the volume to the desired level and then move the mouse between squares A and B to switch between tracks.

## ABX
[ABX method](https://wikipedia.org/wiki/ABX_test) of comparing audio files is a well-known, double-blind comparison method. The benefit of blind testing is the elimination of certain kind of biases. ABX allows the listener to focus on just the audio comparison, eliminating any possible expectation of differences that might be based on visual (or other, non-audio-based) recognition of the source of the audio track.

ABX consists of trying to compare a randomly chosen track (X) to tracks A or B, and to then decide if X track is A or B. If after a reasonable number of tests (15-20) the statistical result is much better than guessing, you can be fairly sure that there is an audible difference that was detectable between these files. To confirm this further, run a few tests, leave some time between them to make it easier on yourself, more relaxed. If the results are consistently much better than guessing, you can conclude that the difference is audible.

Please note that ABX can't prove the negative, that the differences are not audible. But, it can help you decide if the change is easy to detect. If after a number of trials you still can't get to a statistically significant result, you can assume that the difference is at least hard to detect, if not completely undetectable.

## ABX Comparison
Some suggested steps to do an ABX-style comparison:

* Select the desired portion of the track to focus on, set comfortable volume level
* Familiarize yourself with the differences between the two files by doing a sighted A/B comparison, as described above
* If you can't detect a difference while doing a visual A/B comparison, try to find another part of the track that might be more obviously different. Raise the volume a bit, as that might aid in detection
* Once you're comfortable that you can tell the difference in a visual A/B test, it is time to begin ABX:

1. Make sure **Reveal Results** checkbox is *unchecked* before you start, and clear the results box by clicking the red X button
2. Move the mouse over the 'X' square and listen to this track. This is a randomly selected track from A or B. 
3. The goal is to determine if track X is the same as A, or B. If you can't tell immediately, move the mouse to A or B square to compare these to X. You can quickly switch between X and A, X and B by moving the mouse back and forth between the appropriate squares
4. Once comfortable that you know what track X is, press one of the two buttons to make your selection: X=A if you think X is track A, or X=B if you think X is track B
5. Your result will be recorded in the result box, but you will not see if the choice was correct or not until you done with all the trials
6. As soon as you record a result, Comparator will make another random pick, so you can continue the test by repeating steps 2-6.
7. Repeat 15-20 times. This helps keep get a reasonable statistical result, while not being too tiring of a process

When finished with the desired number of trials, click on the **Reveal Results** checkbox. Comparator will show all the results and compute a percent statistic that shows whether or not the result is statistically significant. Often, a 5% or lower statistic is considered significant. If you want to be more strict, less than 1% is a good metric to strive for.

Because of the random nature of X track selection, too few trials can produce a result that looks good, but is not statistically valid. It is important to have a reasonable number of trials, and more than one test to demonstrate that the differences are truly detectable.
___
{% include links.html %}
