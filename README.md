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
```python
# Developed By: HARI PRIYA M
# Register Number: 212224240047

import cv2
import matplotlib.pyplot as plt
from google.colab.patches import cv2_imshow

gray_image = cv2.imread('/content/grayscale-photo-of-dog-lying-on-floor_800.jpg')
color_image = cv2.imread('/content/baby-kittens-in-a-group_800.jpg')
# Resize the images
resized_gray_image = cv2.resize(gray_image, (400, 300)) # Example size, adjust as needed
resized_color_image = cv2.resize(color_image, (400, 300)) # Example size, adjust as needed
cv2_imshow(resized_gray_image)
cv2_imshow(resized_color_image)

import numpy as np
gray_image=cv2.imread('/content/grayscale-photo-of-dog-lying-on-floor_800.jpg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('/content/baby-kittens-in-a-group_800.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

import cv2
from google.colab.patches import cv2_imshow

gray_image = cv2.imread("/content/grayscale-photo-of-dog-lying-on-floor_800.jpg",0)
cv2_imshow(gray_image)
equ = cv2.equalizeHist(gray_image)
cv2_imshow(equ)



```
### Developed By 
### HARI PRIYA M
### 212224240047

## Output:
### Input Grayscale Image and Color Image
<img width="500" height="700" alt="Screenshot 2025-09-17 020819" src="https://github.com/user-attachments/assets/9386847b-c2d4-4ad3-b652-68df9bec5ef2" />



### Histogram of Grayscale Image and any channel of Color Image
<img width="500" height="500" alt="Screenshot 2025-09-17 020843" src="https://github.com/user-attachments/assets/4ff8d717-1bcd-4fce-be36-6528acbdd432" />
<br>
<img width="500" height="500" alt="Screenshot 2025-09-17 020855" src="https://github.com/user-attachments/assets/03ca1e3a-849f-4d6e-ae83-6a33d6b66293" />
<br>
<img width="500" height="500" alt="Screenshot 2025-09-17 020904" src="https://github.com/user-attachments/assets/f18ebc11-7717-47fa-90bb-0e527baa7d6d" />
<br>
<img width="500" height="500" alt="Screenshot 2025-09-17 020914" src="https://github.com/user-attachments/assets/78c5921a-4cd0-4d53-acd4-f104a8871440" />



### Histogram Equalization of Grayscale Image.

<img width="500" height="500" alt="Screenshot 2025-09-17 020936" src="https://github.com/user-attachments/assets/694f9f95-2ab3-4cd7-b07d-24602b7e220e" />

<img width="500" height="500" alt="Screenshot 2025-09-17 021011" src="https://github.com/user-attachments/assets/78aca89d-fc58-4ab0-b1c7-55cf55a04192" />





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
