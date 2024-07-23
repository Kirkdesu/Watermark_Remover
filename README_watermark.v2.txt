Watermark Remover for the Browser

BASIC USAGE:

  The basic usage is to first load an image (or multiple) either by pressing
  the button or drag-and-dropping it onto your browser window. Then load the
  watermark sample by using the respective button, and position it either by
  dragging it with your mouse or using the keyboard arrow keys. Finally, press
  the "Unwatermark" button to get your result.

BATCH MODE:
  
  If you load more than one image, the unwatermarker will enter the batch mode.
  That is, it will go through all the loaded images one after another. Depending
  on whether you have enabled the "Full batch mode" setting, this can happen in
  two ways. If it is enabled, it will automatically go through all files without
  interruption upon clicking "unwatermark" on the first one. During that, the
  watermark will be automatically positioned relative to your selected "default
  watermark position". If "full batch mode" is disabled, it will still go
  through all the selected images, but in a fashion similar to the individual
  unwatermarking. That means, it will stop and give you time to reposition the
  watermark, adjust settings or even load different watermark files, and only
  progress to the next file once your click one of the buttons "unwatermark" or
  "skip" (where that image will *not* be processed at all).
  
FULL DESCRIPTION:

  The following explains in more detail what each button does. Since version
  1.1, some of these are hidden behind the "Show advanced options". (I'm too
  lazy to rework these descriptions to reflect that though.)
  
  "Load Image":
    Loads the image to unwatermark. If you select multiple files, the tool
    will go through them all one after another. You can also drag and drop
    the files onto the window.

  "Load Watermark":
    Load the watermark file to be used. They are the same as the ones from
    FIRE's extractor or tangerine's PhotoShop actions.
  
  "Default watermark position":
    Specifies where the watermark will be put after it has been loaded, so
    you don't have to drag it all over the page to the opposite corner.
    Using it after the watermark has been loaded will have no effect.

  Positioning the Watermark:
    You can drag and drop the watermark once it has been loaded. For fine
    tuning the positioning, use the arrow keys on your keyboard to move it
    by 1px. However, since that might still not be fine enough of an adjust-
    ment for some watermarks, you may hold the CTRL-key while using the arrow
    keys to move in 0.05px steps to *really* get it in the right spot. Also,
    be sure to check out the Automatic Subpixel Alignment option.
    
  "Preview blending mode":
    To help with the positioning, you can switch between "normal" blending
    (the watermark is simply overlayed on top of the image) and "difference"
    blending mode (which works differently and emphasizes misalignment).
    Note that the preview you can see *doesn't* represent the actual un-
    watermarking result.

  "Preview contrast":
    Increase (or decrease) the contrast of the preview. Does not affect the
    final result. Click the spinning arrow symbol to reset it.

  "Preview brightness":
    Increase (or decrease) the brightness of the preview. Does not affect the
    final result. Click the spinning arrow symbol to reset it.
  
  "Transparency threshold":
    Pixels with an alpha value less than this value (= more transparent) will
    not be processed. The reason being, you can't really tell that small
    changes apart, so they don't need to be processed, speeding up the
    unwatermarking a little bit. Plus, most of them stem from JPEG compression
    anyway, meaning they're not really part of the watermark in the first place.

  "Opaque smoothing":
    For some very opaque watermarks (especially JPEG-heavy), there can be ugly
    artefacts in the resulting image. This option tries to hide the worst of
    them by averaging especially opaque pixels with their preceeding pixel.
    The strength/mix of the averaging is determined by how much the alpha is
    over the limit. The default value is high enough to not interfere with
    bilibili's watermark, one of the more common, yet very opaque watermarks.
    As such, the default value will not smooth that strongly, so play around
    with it if you really need it. 255 will disable it.
    Example: https://cdn.discordapp.com/attachments/743513778150178877/779279135796494337/unknown.png

  "Confirm results":
    With this it will not discard source images once they've been unwatermarked,
    but will ask you for confirmation (the buttons will pop up in place of the
    "Unwatermark" button). "Yes" will confirm the changes, save the result
    and move on to the next image (if applicable). "No" will revert to the
    original image, discarding any changes. Useful if the watermark is hard to 
    position.

  "Automatic subpixel alignment":
    The tool will try to adjust the subpixel alignment itself, you just need
    to bring the watermark within 1px distance from its optimal spot (in other
    Words, you still need to adjust pixel accurately). Since it does have
    performance implications for larger watermarks (the code is not very opti-
    mized) and has a possibility to make already perfectly aligned watermarks
    look slightly worse, it is disabled by default.
    
  "Full batch mode":
    If multiple input files are chosen, go through them one after another
    without stopping. Watermark positioning will be determined based on the
    "default watermark position" setting. Start the processing by positioning
    the watermark on the first image and then hitting "unwatermark".
    If disabled, the semi-batch mode will be used, where you can adjust the 
    watermark position for each image individually like normal.
    
  "Save as ZIP in batch mode":
    When running a batch job of either mode (full or semi batch mode), save all
    images bundled into one ZIP file instead of downloading each page
    individually. Pages you "skip" in the semi batch mode will *not* be included
    in the resulting zip.
    
  "Extras":
    Extras are little bonus utilities that can provide added functionality.
    They can either be run on-demand by clicking "play" button on the right of
    the selection, or in some case are executed automatically upon loading of a
    new image. The latter are marked with an asterisk in the list. Currently,
    the following extras are provided:
      - automatic watermark generation for Tencent (ac.qq.com): This will try
          to create a watermark file matching the current image's width and will
          also position it correctly. It is mostly intended for series where
          every page is of different size, or where the size generally is of an
          uncommon size with no good watermark extraction material. But of
          course it cant also be used on commonly sized images. Note however,
          that the watermark generation seems to follow different rules on some
          specific image widths (eg. 2480x) and this feature does not account
          for that.
      - general watermark resizing: can be useful for other sites that resize
          their watermark based on page size. If either target width or height
          are left blank, it will be calculated from the base watermark's aspect
          ratio. Resizing is always done from the source watermark file (loaded
          normally before running this function), so you can resize multiple
          times in a row without having to worry about decreasing image quality.
          Scaling is done using Lanczos filtering providing sharp scaling. Many
          websites use something similar to scale their images but if your files
          happen to be scaled using something else (eg. bilinear interpolation),
          you might end up with visible artefacts.
      - watermark resizing by source size: sometimes it's cumbersome to first
          calculate the watermark size you will need. In that case, this
          variation of the watermark resizing feature can prove useful. You just
          need to enter the size of the watermark's source page and it will
          calculate the target size for you. However, because of rounding
          differences, the results will not always quite fit. Because of that,
          this will print the calculated size for you to use with the other 
          resizing function.
    
  "Watermark alpha adjustment":
    This setting adjusts the watermark's opacity during the unwatermarking (i.e
    not during preview). It can occasionally happen that some watermarks' alpha
    changed between different titles or time frames while the overall appearance
    remained the same. In that case, this setting can help if affected titles
    don't provide sufficient watermark extraction material of their own.

  "Unwatermark":
    When the watermark is in the right spot, click this button to start the
    unwatermarking process. Once done, the unwatermarked image will download
    and if you don't have any other images loaded/queued, it will also be
    shown in the image area.
    File name will be the original file name with "_uwm" appended, as PNG.
    (uwm = UnWaterMarked)

  "Zoom":
    Use "+" and "-" to adjust the zoom level, the spinning arrow to reset it to
    100% (well, not actually 100% in all cases, but the initial zoom level).
    If you're hovering your cursor over the image, you can also hold CTRL while
    scrolling. The option "Pixelated" will tell your browser to use, well,
    pixelated scaling instead of the usually smoother default scaling if that is
    supported.
