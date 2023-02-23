# Image_preprocessing
from skimage.metrics import mean_squared_error
from skimage.io import imread

# Load the two images to be compared
img1 = imread("image1.png", as_gray=True)
img2 = imread("image2.png", as_gray=True)

# Calculate the mean squared error between the two images
mse = mean_squared_error(img1, img2)

# Define a threshold for the similarity score
similarity_threshold = 0.1

# Compare the MSE with the similarity threshold
if mse < similarity_threshold:
    print("The two images are similar.")
else:
    print("The two images are different.")
