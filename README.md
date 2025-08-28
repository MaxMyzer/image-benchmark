# image-benchmark
Benchmarking image file formats

## Motivation
I was browsing the [PEP repository](https://github.com/ENDESGA/PEP), and saw a table comparing image formats in the README. It was missing quite a lot of formats, and only had compression/decompression time for a few formats. I saw there was a PR to fix some of these issues, and a comment linking to [this webpage](https://meow.catt0s.win/test_images/formats/). 

## Why
The goal is to create a program that programmatically benchmarks how different formats perform, and allow users to compare and contrast what the tradeoffs of using a format are.
Note:: There are undoubtedly flaws with the methodology used here. For instance, the libraries used may have outstanding optimizations. 

## What
### Measuring: 
* Compression Time
* Decompression Time
* End File Size
* Compression Ratio
I am considering comparing libraries as well.
### Formats: 
* JPEG [Wiki](https://en.wikipedia.org/wiki/JPEG) [Website](https://jpeg.org/jpeg/)
* PNG [Wiki](https://en.wikipedia.org/wiki/PNG)
  * PNG 3.0
  * APNG [Wiki](https://en.wikipedia.org/wiki/APNG)
* GIF [Wiki](https://en.wikipedia.org/wiki/GIF)
* BMP [Wiki](https://en.wikipedia.org/wiki/BMP_file_format)
* QOI [Wiki](https://en.wikipedia.org/wiki/QOI_(image_format)) [GitHub](https://github.com/phoboslab/qoi) [Website](https://qoiformat.org/)
* FIT [GitHub](https://github.com/open-source-firmware/flat-image-tree)
* PEP [GitHub](https://github.com/ENDESGA/PEP)
* JPEG XL [Wiki](https://en.wikipedia.org/wiki/JPEG_XL) [GitHub](https://github.com/libjxl/libjxl) [Website](https://jpeg.org/jpegxl/)
* HEIF
  * AVIF [Wiki](https://en.wikipedia.org/wiki/AVIF) [Website](https://aomediacodec.github.io/av1-avif/)
* WebP [Wiki](https://en.wikipedia.org/wiki/WebP) [Repo](https://chromium.googlesource.com/webm/libwebp) [Website](https://developers.google.com/speed/webp)
### Test Set:
TODO, trying to come up with a good test set. Looking into items to provide combinations of these qualities:
* Sprites (low colors, small)
  * Alpha
  * Animated with alpha
* Simple Fonts (monochrome, tiny)
* Repetative images (checkerboards and test cards)
* High bit-depth images (HDR)
* Enormous images (space photos?)
* Digital artwork
* "everyday" images
### Caveats
* Present caveats about formats, such as support for HDR, Lossless, multi-frame (animated), maximum colors
* Attempt to render all formats in browser to show limited support 
* How do measure visual quality?
### Variables
* Speed settings (such as faster/slower for less/more compressed images)
* Quality settings (how much can you save with quality reductions?)
  * TODO: How to standardize quality? - JPG compression will look worse than a comperable JXL, for example. Quality settings are not a standard. Perhaps go to qualities to get some percent reduciton in file size will be a good way to do this?
* TODO: Variables specific for formats?
* Add image libraries as part of comparison
  * overall size (including non-STDLIB dependencies)
  * how much do results differ?
