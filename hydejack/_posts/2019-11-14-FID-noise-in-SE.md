---
title: MRI Notes - FID noise in SE sequence?
image: /assets/img/blog/fine_line_artifact.jpg
description: >
  Why there is a fine line in the MR image of SE sequence?
tags: Radiology
---

# MRI Notes: FID noise in SE sequence?
When I was doing the MRI spin-echo experiment, I found there was an obvious fine line at the middle of the final image we obtained
(as shown above). Trust me, I was trying to image a peanut, maybe with some water at the bottom(the bright part). Yes, it is a peanut,
imaged by an old weird MRI scanner with horribly inhomogeneous 0.5T magnetic field. However, even though the scanner was old, it should
never be blamed for the fine line in the middle. Let's find out the true original of this artifact and clear the scanner of this noise.

## Spin-echo sequence
To start with, let's have a quick look at what is spin-echo sequence.
