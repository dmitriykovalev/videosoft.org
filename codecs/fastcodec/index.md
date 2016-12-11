---
layout: page
title: FastCodec
menu: main
---

[![Download Fastcodec]({{site.baseurl}}/assets/download-big.gif)][download]

## Overview

FastCodec is a fast lossless video codec. Compression algorithm is relatively simple and fast.

* Lossless and lossy (near lossless) compression.
* Fast preview mode decompression.
* Lossless compression requires frame width and height must be a multiple of 4. Lossy compression requires frame height is multiple of 4 and frame width is multiple of 8.
* Supported input and output formats: YUY2/YUNV/V422/YUYV, YVYU, UYVY/Y422/UYNV, RGB24, RGB32.

Some performance results can be found in [MSU Lossless Video Codecs Comparison ‘2007][comparison].

## Description

<img style="padding-left: 20px;float: right;" src="{{site.baseurl}}/assets/fastcodec-help.jpg">


**I. CPU detection.** Codec detects supported CPU instruction sets in runtime and chooses fastest algorithm implementation.

**II. Compression settings.** YUV compression is always lossless. RGB compression can be (A)
absolutely lossless (mathematically identical) and (B) visually lossless (human eye cannot see a difference). Visually lossless RGB results in slightly better compression.

**III. Decompression settings.** Preview mode (A) is a special feature for super fast decompression with low image quality. Could be helpful on slow machines.</p>

**IV. Logging.** Codec can write some information to the specified file while compression/decompression. That is mostly used for debugging purposes and should be disable for the best performance.

[download]: {{site.baseurl}}/res/download/codecs/fastcodec/fastcodec-setup.exe
[comparison]: http://compression.ru/video/codec_comparison/lossless_codecs_2007_en.html
