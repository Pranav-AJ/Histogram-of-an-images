# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```

# Developed By: A.J.PRANAV
# Register Number: 212222230107
```
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('flower.jpeg')
color_image = cv2.imread('tree.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
gray_image=cv2.imread('flower.jpeg')
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()


color_image=cv2.imread('tree.jpg')
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()
```
```
gray_image = cv2.imread("flower.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### Input Grayscale Image and Color Image

![image](https://github.com/user-attachments/assets/184b148d-9a93-477a-8ab4-0c7ede076782)
![image](https://github.com/user-attachments/assets/ab513c95-3172-4194-b83e-d44425047e40)


### Histogram of Grayscale Image and any channel of Color Image
#### Grayscale image
![image](https://github.com/user-attachments/assets/7c8e7c69-74ab-4fdb-a513-74aebe420218)
![image](https://github.com/user-attachments/assets/63d99653-60f7-45ab-a507-a103ae987668)
#### color image
![image](https://github.com/user-attachments/assets/74fd929a-3aba-4179-b1f4-fa2b042f2039)

![image](https://github.com/user-attachments/assets/e3e8d205-c706-439c-84ab-415aede2ccfa)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/5b93c434-7029-413a-92a7-51136f2c7220)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
