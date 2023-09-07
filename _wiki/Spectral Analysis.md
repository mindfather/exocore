---
published: true
subtitle:
date: 2023-09-07
tags: music media-node
---

# Spectral Analysis
As the price of data storage becomes cheaper, it starts to become a lot easier to keep **lossless** files of the music that we wish to preserve. It's important to ensure in one's journey of music collection that all "lossless" files obtained are actually so, and not transcodes.

![[bitches brew spek.png]]

Spectral Analysis is a powerful tool in determining whether or not you're dealing with a transcode, or an actual lossless file, but it's not an exact method. you can generate such a graph using [Audacity](https://audacity.sourceforge.net) or [Spek](https://spek.cc).

`mp3` encoded files generally apply a low-pass filter to the music to reduce the file size for compression, with cutoffs described in the table below:

| bitrate | cutoff  |
| ------- | ------- |
| 320kbps | 20kHz   |
| 256kbps | 19.5kHz |
| 192kbps | 19kHz   |
| 128kbps | 16.5kHz | 

It's important to note that `mp3` files will generally have a "shelf" at 16kHz due to the LAME encoder's [-Y switch](https://wiki.hydrogenaud.io/index.php?title=LAME_Y_Switch). This allows the encoder to encode frequencies `>= 16kHz` more coarsely to prevent disproportional increases in bitrate.

![[Sacrifice spek.png]]

The reason I say that LAME "generally applies a low-pass filter" is because there exist encodes which do no such thing, and could easily pass as lossless to the eye. This mostly applies to electronic music:

![[Inversion spek.png]]

![[bebetunes spek.png]]

Conversely, the artist might just send their song through a low-pass filter by choice and still release flac files for it, or they might use a sample which is was not lossless. It's important to use your better judgement in determining whether a spectrograph looks correct for the music in question.

![[big up menace x spek.png]]

Music which was recorded in an analog-only environment is much easier to judge using spectral analysis.

![[aja lossless.png]]

![[aja lossy.png]]

The main tell of lossy -> lossy transcodes is the fact that the peak frequencies will seem boosted when compared to a more proper encode.

![[Pasted image 20230907121600.png]]

Yet this is something that is encountered a bit less in modern times as we are able to seek out lossless files more often with less concern for storage space.

That's pretty much it for my scattered tips for identifying properly encoded music, or proper lossless files. It's important to start this early when building out a music library as checking your files will only get more and more tedious as the library is built up. In the future, I'll explain how you can properly tag and normalize filenames/folder structures for your music.