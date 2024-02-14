# COLOR_CONVERSIONS_OF-IMAGE

## AIM


#### To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv) To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:

### Anaconda - Python 3.7

## Algorithm:


### Step 1

Choose an image and save it as a filename.jpg 

### Step 2

Use imread(filename, flags) to read the file.


### Step 3

Use imshow(window_name, image) to display the image.

### Step 4

Use imwrite(filename, image) to write the image.

### Step 5

End the program and close the output image windows.


### Step 6

Convert BGR and RGB to HSV and GRAY

### Step 7

Convert HSV to RGB and BGR

### Step 8

Convert RGB and BGR to YCrCb

### Step 9

Split and Merge RGB Image


### Step 10

Split and merge HSV Image

 
Developed By: DINESH KUMAR R

Register Number: 212222110010


#### IMAGE 

<img src='raw.jpg'>

## Program:


### (i) Read and display the image
 ```py
#Read and display the image
import cv2
image=cv2.imread('ex01.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('dinesh',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output:

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/e33b0c40-9e0b-4114-a01b-ed6f9816662f)

## Program:

### (ii) Write the image

```py
#Write the image
import cv2
image=cv2.imread('ex01.jpg',0)
cv2.imwrite('demos.jpg',image)

```
### Output

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/ccfd6b68-3b7f-4170-9d1c-9188a5003106)


## Program:

### (iii) Shape of the Image

```py
#Shape of the Image
import cv2
image=cv2.imread('ex01.jpg',1)
print(image.shape)
```


### Output

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/bf6fb231-b4ff-4a30-8ea3-38c4cb656749)


## Program:

### (iv) Access rows and columns
```py
#Access rows and columns
import random
import cv2
image=cv2.imread('ex01.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/3e039b4b-ea17-4ff0-b2a0-49f2c3f21e30)


## Program:

### (v) Cut and paste portion of image
```py
#Cut and paste portion of image
import cv2
image=cv2.imread('ex01.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/777b3d8c-665a-427f-be83-101c4ee1a982)

## Program:

### (vi) BGR and RGB to HSV and GRAY
```py
#BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('ex01.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Original Image

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/d580dfac-dbf5-43ee-a76c-58b7bc0ac70b)


### Output

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/84c8a1df-0db9-4b7e-ba3a-32d544030ab8)

## Program:

### (vii) HSV to RGB and BGR

```py
#HSV to RGB and BGR
import cv2
img = cv2.imread('ex01.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Original HSV

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/7a27920b-a8f1-4832-ab0f-43412a313c7f)


### Output
![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/a5795dc3-9e99-468f-8b34-8406276088f1)




## Program:

### (viii) RGB and BGR to YCrCb
```py

#RGB and BGR to YCrCb
import cv2
img = cv2.imread('ex01.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output


![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/d4fede5c-ecad-4a2d-ab4d-6f26b88a8b93)


## Program:

### (ix) Split and merge RGB Image
```py
#Split and merge RGB Image
import cv2
img = cv2.imread('ex01.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output

#### Channels

![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/a9bd3428-22be-4cef-b2d2-fd7ea6e30a69)


#### Merged RGB


![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/dee12921-d177-41e8-89f1-a0130203c4bd)


## Program:

### (x) Split and merge HSV Image
```py
#Split and merge HSV Image
import cv2
img = cv2.imread("ex01.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output

### Merged HSV


![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/3b351b7f-cbe3-439e-950f-1b7799a04563)


### Splitted


![image](https://github.com/DINESH18032004/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/ed8b3fa0-9186-47cc-b6aa-40da2dbc7d31)


## Result:
#### Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
