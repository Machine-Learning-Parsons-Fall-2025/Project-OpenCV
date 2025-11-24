## copied from other Project-OpenCV fork:
### Progress Made:

- Imported images and started to process with openCV
    - learned that you usually detect a white shape on a black background in openCV
    - added border along edge of images 
    - tooled around with erosion/dilation 
- things I need to solve:
    - not all images are greyscale/go through the black/white filtering and color inverting properly
    - how much/when should I dilate/erode?

Trying to use openCV to process and detect shapes in my images. I'm running into more difficulty than expected in setting up my images for detection. I thought they would all be black and white, but apparently they're shaded, and some are not greyscale at all. The findContours() / finding the outline code that Thiago gave to me. I'm having success with some kamon, not that much with others. Many kamon have delicate or thin, low-res lines, which can get eroded away and end up "breaking" the outline of the kamon. This means there is no longer a dominant contour, and the kamon is broken up into a bunch of little shapes. I'm not sure if I want this.

I think once I punch through this image processing step, the next steps (maybe dimensionality reduction, and then K-means clustering, I think) should be more straightforward.

Maybe try simpler blob detection?
https://opencv.org/blog/blob-detection-using-opencv/