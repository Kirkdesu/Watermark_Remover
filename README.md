# Watermark_Remover

[Readme Português](https://kirkdesu.github.io/Watermark_Remover/UNWATERMARKER.html)

[Readme English](https://kirkdesu.github.io/Watermark_Remover/UNWATERMARKER.html)

https://kirkdesu.github.io/Watermark_Remover/

Não sou o criador, apenas criei o repositório

I'm not the creator, I just created the repository


# Watermark Extractor

https://kirkdesu.github.io/Watermark_Remover/EXTRACTOR.html

## Usage

You will need two samples of the watermark on different uniform backgrounds. These two samples must come from your image source; editing in a different background yourself will not give you the results you want. Once you have your two samples, the following steps are necessary:

### Load Image 1 & Load Image 2
Load the respective samples into the extractor. Image 2 will be overlaid on top of Image 1 with an opacity of 50%.

If you have the "contrast stretch" option ticked, the images you see will be edited for better visibility of very light (or dark) watermarks. This is done by stretching the color range of the loaded image to the full range between black and white. This option only works well if you have cropped your samples to only the watermarks prior to loading them into here.

### Set the Background Colors
For optimal results, the background colors should be specified correctly. With the "Image # BG color" buttons, you can set the color using your system's color chooser menu. The magnifying glass next to it will function as a color picker/dropper, similar to those of usual image editing programs. This means that you just have to click the magnifying glass icon and then click a spot in the image where the background color is clearly visible, and the tool will select that color you have clicked on. (I couldn't find a unicode dropper symbol, hence the magnifying glass lol.)

### Position the Images to Have the Watermarks Line Up
As with the watermark remover, drag and drop it for coarse movement and use the arrow keys for fine-tuning. The various blend modes and filters might help you.

### Position the Extraction Box
You will probably have noticed the blue box by now. It is used to mark the area from which the watermark shall be extracted. Position it by drag and drop (no arrow keys here) and resize it by using the bottom right corner. If it goes off the page, that shouldn't pose an issue and will be clipped to the closest points where both images are visible again.

### Click "Extract"
The extracted watermark will download (unfortunately no preview here).

## Additional Notes
The watermark files will be compatible with FIRE's tools.
Thank you for the math behind this, FIRE.

---

# Watermark Remover

https://kirkdesu.github.io/Watermark_Remover/UNWATERMARKER.html

## Basic Usage

The basic usage is to first load an image (or multiple) either by pressing the button or drag-and-dropping it onto your browser window. Then load the watermark sample by using the respective button, and position it either by dragging it with your mouse or using the keyboard arrow keys. Finally, press the "Unwatermark" button to get your result.

## Batch Mode

If you load more than one image, the unwatermarker will enter the batch mode. Depending on whether you have enabled the "Full batch mode" setting, this can happen in two ways:

1. If "full batch mode" is enabled, it will automatically go through all files without interruption upon clicking "unwatermark" on the first one. The watermark will be automatically positioned relative to your selected "default watermark position".
2. If "full batch mode" is disabled, it will still go through all the selected images, but in a fashion similar to individual unwatermarking. It will stop and give you time to reposition the watermark, adjust settings, or even load different watermark files, and only progress to the next file once you click one of the buttons "unwatermark" or "skip" (where that image will *not* be processed at all).

## Full Description

The following explains in more detail what each button does. Since version 1.1, some of these are hidden behind the "Show advanced options".

### Load Image
Loads the image to unwatermark. If you select multiple files, the tool will go through them all one after another. You can also drag and drop the files onto the window.

### Load Watermark
Load the watermark file to be used. They are the same as the ones from FIRE's extractor or tangerine's Photoshop actions.

### Default Watermark Position
Specifies where the watermark will be put after it has been loaded, so you don't have to drag it all over the page to the opposite corner. Using it after the watermark has been loaded will have no effect.

### Positioning the Watermark
You can drag and drop the watermark once it has been loaded. For fine-tuning the positioning, use the arrow keys on your keyboard to move it by 1px. You may hold the CTRL-key while using the arrow keys to move in 0.05px steps to *really* get it in the right spot. Check out the Automatic Subpixel Alignment option.

### Preview Blending Mode
To help with the positioning, you can switch between "normal" blending (the watermark is simply overlaid on top of the image) and "difference" blending mode (which works differently and emphasizes misalignment). Note that the preview you can see *doesn't* represent the actual unwatermarking result.

### Preview Contrast
Increase (or decrease) the contrast of the preview. Does not affect the final result. Click the spinning arrow symbol to reset it.

### Preview Brightness
Increase (or decrease) the brightness of the preview. Does not affect the final result. Click the spinning arrow symbol to reset it.

### Transparency Threshold
Pixels with an alpha value less than this value (= more transparent) will not be processed. This speeds up the unwatermarking a little bit and is useful for small, unnoticeable changes.

### Opaque Smoothing
For very opaque watermarks (especially JPEG-heavy), there can be ugly artefacts in the resulting image. This option tries to hide the worst of them by averaging especially opaque pixels with their preceding pixel. The default value is high enough to not interfere with common watermarks. Play around with it if needed. 255 will disable it.

### Confirm Results
This option will not discard source images once they've been unwatermarked but will ask you for confirmation. "Yes" will confirm the changes, save the result, and move on to the next image. "No" will revert to the original image, discarding any changes. Useful if the watermark is hard to position.

### Automatic Subpixel Alignment
The tool will try to adjust the subpixel alignment itself. You still need to adjust pixel accurately within 1px distance from its optimal spot. Disabled by default due to performance implications for larger watermarks.

### Full Batch Mode
If multiple input files are chosen, go through them one after another without stopping. Watermark positioning will be determined based on the "default watermark position" setting. Start the processing by positioning the watermark on the first image and then hitting "unwatermark". If disabled, the semi-batch mode will be used.

### Save as ZIP in Batch Mode
When running a batch job, save all images bundled into one ZIP file instead of downloading each page individually. Pages you "skip" will *not* be included in the resulting ZIP.

### Extras
Extras are little bonus utilities that provide added functionality:

- **Automatic watermark generation for Tencent (ac.qq.com):** Creates a watermark file matching the current image's width and positions it correctly.
- **General watermark resizing:** Useful for sites that resize their watermark based on page size. Scaling is done using Lanczos filtering.
- **Watermark resizing by source size:** Calculates the target size based on the watermark's source page size.

### Watermark Alpha Adjustment
Adjusts the watermark's opacity during the unwatermarking process. Useful if the watermark's alpha changed between different titles or time frames.

### Unwatermark
Starts the unwatermarking process. The unwatermarked image will download with "_uwm" appended to the file name as a PNG. 

### Zoom
Use "+" and "-" to adjust the zoom level, the spinning arrow to reset it. You can also hold CTRL while scrolling to adjust the zoom level. The option "Pixelated" will use pixelated scaling instead of the smoother default scaling if supported.
