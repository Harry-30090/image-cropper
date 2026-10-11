# Image Slicer — 3:2 → 1:2 × 3

A simple, browser-based image slicer that splits a single image into **three equal vertical sections**, producing three separate images for download.

## Features

* **Upload an image** from your device.
* **Split into three sections** of equal width.
* **Preview the results** directly in your browser.
* **Download each section** individually as a JPEG image.
* **No installation required** — runs entirely in your browser.
* **No server required** — images are processed locally using HTML Canvas.

## How to Use

1. Download or clone this repository.
2. Open the HTML file in a web browser.
3. Click the file selection button and choose an image.
4. Wait for the three previews to appear.
5. Click `Download 1`, `Download 2`, or `Download 3` to save each section.

## How It Works

The tool uses the HTML Canvas API to divide the uploaded image into three equal vertical sections.

For an input image with dimensions \(W \times H\), each output has dimensions:

* **Width:** \(W / 3\)
* **Height:** \(H\)

The image is divided from left to right:

| Output  | Source region |
| ------- | ------------- |
| Image 1 | Left third    |
| Image 2 | Middle third  |
| Image 3 | Right third   |

Each output is exported as a JPEG image at 95% quality.

## Technologies

* HTML5
* CSS3
* JavaScript
* HTML Canvas API

No external libraries or dependencies are required.

## Limitations

* The image is divided into three equal-width sections, regardless of its original aspect ratio.
* The tool does not resize or crop images to enforce a specific aspect ratio.
* Output images are saved as JPEG files, even when the original image uses another format.
* Each section is downloaded separately; there is no ZIP export.
* If the source image's width is not divisible by three, the output canvas dimensions may be fractional and subject to browser rounding.

## Privacy

All image processing takes place locally in your browser. The code does not upload images to a server.
