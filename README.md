# PSYEX-PSNR: Psychovisually Exotic PSNR

## Overview

PSYEX-PSNR or Psychovisually Exotic PSNR is a PSNR based metric that takes the metric's main strength(low computational complexity) and extends it further to make it correlate much more heavily with the Human Visual System(HVS) and general human opinions.

This is based on multiple parts to make the metric as robust as possible:

1. All operations are computed in the XYB color space instead of YCbCrto get a more perceptually accurate color space and to more heavily penalize common color artifacts.

2. Frequency weighted PSNR using a custom built contrast sensitivity function.

3. Additional weighting by using the basis of activity masking through edge detection(to counteract ringing and blur artifacts).

4. Multi-scale PSNR analysis to more properly take into account viewing distance and object importance size. Downscaling is done in linear light.

5. For all of these frames, multiple norms are computed for the various psy weighted PSNR scores.

Currently, all of these are theoritical feature implementations, and will need further refinement as the program gets built. This is not to even mention the subjective testing that needs to be done.

This program is based and inspire by works in the JPEG-XL standard(XYB and the frequency weightings), rav1e(activity masking), PSNR HVS, and ssimulacra2 (downscaling in linear light and the existence of PNXR in the first place).

## Build Instructions

### Toolchain: Rust
PXNR requires Rust XXX to build.

### Release binary
TBD later, as PXNR could either be implemented as a library or as a library+CMD UI.
