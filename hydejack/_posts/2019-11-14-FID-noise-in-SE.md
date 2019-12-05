---
title: MRI Notes - FID noise in SE sequence?
image: /assets/img/blog/fine_line_artifact.jpg
description: >
  Why is there a fine line in the peanut MR image of SE sequence?
tags: Radiology
---

# MRI Notes: FID noise in SE sequence?
When I was doing the MRI spin-echo experiment, I found there was an obvious fine line at the middle of the final image we obtained
(as shown above). Trust me, I was trying to image a peanut, maybe with some water at the bottom(the bright part). Yes, it is a peanut,
imaged by an old weird MRI scanner with horribly inhomogeneous 0.5T magnetic field. However, even though the scanner was old, it should
never be blamed for the fine line in the middle. Let's find out the true origin of this artifact and exonerate the scanner.

## Spin-echo Sequence
To start with, let's have a brief look at what spin-echo(SE) sequence is.

SE sequence is a widely used MRI sequence in clinical application. The main feature of it is that it uses a 180° RF impulse to flip the transverse component of the magnetization to another side and thus refocus the phase after dispersion. In other word, the 180° impulse acts like a starting gun which requires all protons to turn around halfway. Therefore, those fast runners who used to lead now have to chase for those slow runners for the same distance. 

![SE_sequence](/assets/img/blog/spin-echo-sequence.jpg)
<center><font size="2">SE sequence</font></center>

**Advantages of SE sequence**  
Theoretically, it can eliminate the extra phase dispersion due to magnetic field's inhomogenity, which means, the time constant of transverse relaxation would be T2 instead of T2* in gradient-rephase sequence. Thus, the signal intensity will be higher during signal acquisition.


## Imperfection of the 180° impulse
Then what is wrong with the SE sequnce now that it is so useful? 

We know that it is impratical to perform an infinitely long RF impulse. We cut it off into finite time and sacrifice its frequncy profile correspondingly. This is how the real frequency spectrum looks like:

**Gonna be an image here**

Therefore, we can see not all protons in the selected slice can be flipped exactly 180°, while those who are filpped bigger or smaller than 180°, will remain a transverse component on XOY plane. And eventually, this residual will induce an FID signal into signal acquisition.

## From FID signal to the fine line
Then, what does the FID signal have to do with the fine line? Let's deduce their relationship step by step on MATLAB.

To make things easier, let's assume we are now imaging a homogeneous object in the middle of the FOV.
### Setting the parameters
First, let's set some parameters of the object we are imaging and the image we are expecting to acquire.
