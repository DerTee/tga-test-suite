Sourced from https://github.com/image-rs/image/tree/master/tests/images/tga/testsuite

---

TrueVision TGA (a.k.a. Targa) 2.0 conformance suite

Official format specification, sample images and utilitiesriginally been publicly available, free of
charge and under no specific licensing terms, from TrueVision, Inc.'s  FTP
server at the following URL:

ftp://ftp.truevision.com/pub/TGA.File.Format.Spec/PC.Version/

All of the material contained here is therefore copyright to TrueVision, Inc.,
unless otherwise stated.

But has been removed in the proceedings of Pinnacle Systems' acquisition of
TrueVision, Inc., as outdated. However, a back-up of these files is available
here:

http://googlesites.inequation.org/tgautilities

---

All the images in this folder have a resolution of 128x128 pixels.

Here's some help for decyphering the file names:
 - "c"/"u" at the beginning is for compressed/uncompressed
 - "bw" in second place is for black and white
 - "tc" in second place is for true color
 - "cm" in second place is for color mapped, which in practice seems to mean 256 colors and 16 bits per palette entry (but both number of colors and bit depth can in principle be specified differently per file)
 - the numbers at the end are the bits per pixel


Additional information about the files:

| File      | Size   | Compression | Bits per pixel | Channels per pixel | Alpha bit depth | Color mapped | Order top to bottom | Order right to left | Support in applications |
| ----      | ----   | ----------- | -------------- | ------------------ | --------------- | ------------ | ------------------- | ------------------- | ------------------------------- |
| cbw8.tga  |  8.759 | RLE         |  8             | 1                  | -               | No           | No                  | No                  | GIMP 3.0.0-1: Yes, Krita 5.2.9: Yes |
| ccm8.tga  |  9.271 | RLE         |  8             | 1                  | -               | Yes          | No                  | No                  | GIMP 3.0.0-1: Yes, Krita 5.2.9: No  |
| ctc24.tga | 21.047 | RLE         | 24             | 3                  | -               | No           | No                  | No                  | GIMP 3.0.0-1: Yes, Krita 5.2.9: Yes |
| ubw8.tga  | 21.047 | None        |  8             | 1                  | -               | No           | No                  | No                  | GIMP 3.0.0-1: Yes, Krita 5.2.9: Yes |
| ucm8.tga  | 21.559 | None        |  8             | 1                  | -               | Yes          | No                  | No                  | GIMP 3.0.0-1: Yes, Krita 5.2.9: No  |
| utc16.tga | 41.527 | None        | 16             | 3 or 4 (ref 1)     | 1 Bit           | No           | No                  | No                  | GIMP 3.0.0-1:  No, Krita 5.2.9: Partial, no alpha |
| utc24.tga | 62.007 | None        | 24             | 3                  | -               | No           | No                  | No                  | GIMP 3.0.0-1: Yes, Krita 5.2.9: Yes |
| utc32.tga | 82.487 | None        | 32             | 3 or 4 (ref 2)     | 8 Bit           | No           | No                  | No                  | GIMP 3.0.0-1:  No, Krita 5.2.9: Partial, no alpha |

(Ref 1) [R5G5B5](https://en.wikipedia.org/wiki/High_color#15-bit_high_color) but the alpha/interrupt/overlay bit seems to be unsupported in modern software at the time of writing this (2025-03-27)
(Ref 2) The TGA specification says that the fourth byte is an attribute bit field: "The attribute bit field is often called the Alpha Channel, Overlay Bit(s) or Interrupt Bit(s)."