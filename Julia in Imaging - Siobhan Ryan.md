
Julia is a high-level, high-performance dynamic programming language for technical computing, with syntax that is familiar to users of other technical computing environments.

###Image packages in Julia 
Julia has a few packages aimed at image processing. We’ll start by looking at the **TestImages package**, which hosts a selection of sample images, then briefly visit the **ImageView** package before moving onto the Images package, which implements a range of functions for image manipulation.
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
The result is a data matrix where each row is an image instance and each column is the value for a specific pixel in the image. Each column is also interpreted as a feature.

These steps can be combined into a single function allowing us to easily repeat the process for other images. Note that we can access the string representation of a variable with syntax *"$(var)"* or *"$var"*.


<pre><code>
typeData could be either "train" or "test.
labelsInfo should contain the IDs of each image to be read
The images in the trainResized and testResized data files
are 20x20 pixels, so imageSize is set to 400.
path should be set to the location of the data files.

function read_data(typeData, labelsInfo, imageSize, path)
 #Intialize x matrix
 x = zeros(size(labelsInfo, 1), imageSize)

 for (index, idImage) in enumerate(labelsInfo["ID"]) 
  #Read image file 
  nameFile = "$(path)/$(typeData)Resized/$(idImage).Bmp"
  img = imread(nameFile)

  #Convert img to float values 
  temp = float32sc(img)

  #Convert color images to gray images
  #by taking the average of the color scales. 
  if ndims(temp) == 3
   temp = mean(temp.data, 1)
  end
    
  #Transform image matrix to a vector and store 
  #it in data matrix 
  x[index, :] = reshape(temp, 1, imageSize)
 end 
 return x
end

</pre></code>

Training and test matrices can now be loaded using function read_data(). Information about the labels can be read using the *readtable()* function :

<pre><code>
imageSize = 400 # 20 x 20 pixel

Set location of data files, folders
path = ...

Read information about training data , IDs.
labelsInfoTrain = readtable("$(path)/trainLabels.csv")

Read training matrix
xTrain = read_data("train", labelsInfoTrain, imageSize, path)

Read information about test data ( IDs ).
labelsInfoTest = readtable("$(path)/sampleSubmission.csv")

Read test matrix
xTest = read_data("test", labelsInfoTest, imageSize, path)
<\pre><\code>
***
###How  Julia compares to matlab for image compression

Red ,Green and Blue.

| Colour        | Size of matrix| Actual size   |
| ------------- |:-------------:| -------------:|
| Red           | mxn           | 500x700       |
| Blue          | mxn           | 500x700       |
| Green         | mxn           | 500x700       |
