Task:
Draw Lines for the coins that fall under the same straight line! (Vertical)
You have to use OpenCV Algorithm to detect the coins

Procedure:
1)The given image is converted into .png format and resized to 400x600

2)Image is converted into grayscale.
	2a)Apply pyramid mean shift filtering to help the accuracy of our thresholding 		   step.

3)Since the background is white , applied threshold and inverted it. 
	3a) There is a bit of noise in this image (i.e., small blobs), cleaned it up by 		performing a series of erosions and dilations.

4)Constructed a mask for just the current label ( labels  stores a unique integer for each blob in thresh)
	4a)Applied contours in bright areas (coins)

5)Found the center of the countour 
	5a) Formed clusters of x coordinates (Vertical lines)
	5b) Draw lines using the mean of the clusters of x coordinates

Note: Since the coins are of different shapes lines cutting exactly through middle of the coin is not possible
