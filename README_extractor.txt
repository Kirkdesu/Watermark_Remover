Watermark Extractor for the Browser

Usage:

  You will need two samples of the watermark on different uniform backgrounds. 
  These two samples must come from your image source, editing in a different 
  background yourself will not give you the results you want. Once you 
  have your two samples, the following steps are necessary:
  
  Load Image 1 & Load Image 2:
    Load the respective samples into the extractor. Image 2 will be overlayed 
    ontop of image 1 with an opacity of 50%.
    
    If you have the "contrast stretch" option ticked, the images you see
    will be edited for better visibility of very light (or dark) watermarks.
    This is done by stretching the color range of the loaded image to the full
    range between black and white. This option only works well if you have
    cropped your samples to only the watermarks prior to loading them into here.
  
  Set the background colors:
    For optimal results, the background colors should be specified correctly. 
    With the "Image # BG color" buttons, you can set the color using your 
    system's color chooser menu. The magnifying glass next to it will function 
    as a color picker/dropper, similar to those of usual image editing programs.
    This means that you just have to click the magnifying glass icon and then 
    click a spot in the image where the background color is clearly visible, and
    the tool will select that color you have clicked on.
    (I couldn't find a unicode dropper symbol, hence the magnifying glass lol.)
  
  Position the images to have the watermarks line up:
    As with the watermark remover, drag and drop it for coarse movement and 
    use the arrow keys for finetuning. The various blend modes and filters might
    help you.
  
  Position the extraction box:
    You will probably have noticed the blue box by now. It is used to mark the 
    area from which the watermark shall be extracted. Position it by drag and 
    drop (no arrow keys here) and resize it by using the bottom right corner. 
    If it goes off the page, that shouldn't pose an issue and will be clipped 
    to the closest points where both images are visible again.
  
  Click "Extract":
    The extracted watermark will download (unfortunately no preview here).

Additional notes:

  The watermark files will be compatible to FIRE's tools.
  Thank you for the math behind this, FIRE.
