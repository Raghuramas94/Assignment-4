# import the necessary packages
import numpy as np
from urllib.request import urlopen
import cv2
from matplotlib import pyplot as plt

# METHOD #1: OpenCV, NumPy, and urllib
def url_to_image(url):
	# download the image, convert it to a NumPy array, and then read
	# it into OpenCV format
	resp = urlopen(url)
	image = np.asarray(bytearray(resp.read()), dtype="uint8")
	image = cv2.imdecode(image, cv2.IMREAD_COLOR)
 
	# return the image
	return image
  
  image = url_to_image("https://fontsarena-cd5e.kxcdn.com/wp-content/uploads/2019/04/helvetica-now-font-400x364.png")
  
  from google.colab.patches import cv2_imshow #importing images through cv2_imshow
cv2_imshow(image) 

from google.colab.patches import cv2_imshow #importing images through cv2_imshow
cv2_imshow(image) 

cv2_imshow(edges) #printing the image with only the edges separated from the image

#kernel = np.ones((3,3),np.float32)/25
kernel = np.float32([[1,-1,1],[-1,0,1],[1,0,-1]])  #Blur kernel as it has blurred the image with respect to the background

dst = cv2.filter2D(image,-1,kernel)
cv2_imshow(dst)

#kernel = np.ones((3,3),np.float32)/25
kernel = np.float32([[-1,0,1],[1,0,1],[1,1,1]]) #this acts as a blur kernel as it has blurred the image along with the background

dst = cv2.filter2D(image,-1,kernel)
cv2_imshow(dst)

#kernel = np.ones((3,3),np.float32)/25
kernel = np.float32([[-1,0,1],[-1,0,1],[-1,0,1]]) #vertical edge detector

dst = cv2.filter2D(image,-1,kernel)
cv2_imshow(dst)

#kernel = np.ones((3,3),np.float32)/25
kernel = np.float32([[-1,0,1],[-1,0,1],[-1,0,1]]) #vertical edge detector

dst = cv2.filter2D(image,-1,kernel)
cv2_imshow(dst)

#kernel = np.ones((3,3),np.float32)/25
kernel = np.float32([[4,1,-3],[-2,-1,1],[-3,0,3]]) #Sharpen kernel , as the image is sharpened when compared to its background

dst = cv2.filter2D(image,-1,kernel)
cv2_imshow(dst)

#kernel = np.ones((3,3),np.float32)/25
kernel = np.float32([[-2,1,2],[-3,-1,3],[-2,1,2]]) #Identity function as it is the same as the original image. Here the image is convolved with the kernel of the same magnitude and of the opposite sign

dst = cv2.filter2D(image,-1,kernel)
cv2_imshow(dst)
