# image-benchmark
Benchmarking image file formats

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
* JPEG XL [Wiki](https://en.wikipedia.org/wiki/JPEG_XL) [GitHib](https://github.com/libjxl/libjxl) [Website](https://jpeg.org/jpegxl/)
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
