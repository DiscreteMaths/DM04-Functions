
Julia is a high-level, high-performance dynamic programming language for technical computing, with syntax that is familiar to users of other technical computing environments.

###Image packages in Julia 
Julia has a few packages dedicated to image processing. We’ll start by looking at the **TestImages package**, which hosts a selection of sample images, then briefly visit the **ImageView** package before moving onto the Images package, which implements a range of functions for image manipulation.
***
###Testimages package
The TestImages package currently provides 25 sample images, which form a convenient basis for experimentation.
**Step 1**
We’ll load the archetypal test image.
**Step 2**
Of course, now that we’ve loaded that image, we’ll want to take a look at it. To do that we’ll need the **ImageView package**.
**Step 3**
You can optionally specify the pixel spacing as a parameter to *view()*, which then ensures that the aspect ratio of the image is conserved on resizing. There are numerious tricks associated with *view()*: you can click-and-drag within the image to zoom in on a particular region;various simple transformations (flipping and rotation) are possible; images can be annotated and multiple images can be arranged on a canvas for simultaneous viewing.
###Image representation
Outside of the test images, an arbitrary image file can be loaded using **imread()** from the Images package. Naturally, there are also functions for writing images, **imwrite()** and **writemime()**.Training and test matrices can now be loaded using function **read_data()**. Information about the labels can be read using the **readtable()** function:

###Imread command and colour matrices
**imread()** allows us to read the image. **float32sc()** changes the image into real values.The default representation for the Image object tells us its dimensions, storage type and colour space. The result could be a single matrix if the image is black/white, or a triple array that contains three matrices representing each color **(Red, Green, Blue)**. 
It is easier to work with images with the same representation, so we convert all of the color images to grayscale by averaging the values across the three color matrices.The result is a single matrix per image. Changing each image matrix into a vector allows us to save all results in a single matrix that contains the data for all images. The result is a single matrix per image. 


***

<pre><code>

img = imread(nameFile)
temp = float32sc(img)
if ndims(temp) == 3
 temp = mean(temp.data, 1)
end
</code></pre>
 ***
The result is a single matrix per image. Changing each image matrix into a vector allows us to save all results in a single matrix that contains the data for all images.
<pre><code>
x[i, :] = reshape(temp, 1, imageSize)
</code></pre>

***

***
###How  Julia compares to matlab for image compression

Red ,Green and Blue.

| Colour        | Size of matrix| Actual size   |
| ------------- |:-------------:| -------------:|
| Red           | mxn           | 500x700       |
| Blue          | mxn           | 500x700       |
| Green         | mxn           | 500x700       |
