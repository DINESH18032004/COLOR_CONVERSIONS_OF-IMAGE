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

 python
Developed By: DINESH KUMAR R
Register Number: 212222110010


#### IMAGE 

<img src='raw.jpg'>

## Program:


### (i) Read and display the image
 ```py
#Read and display the image
import cv2
image=cv2.imread('exp01.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('dinesh',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output:
![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/4a238b1e-0717-445a-8018-b2fa53b6ad15)


## Program:

### (ii) Write the image

```py
#Write the image
import cv2
image=cv2.imread('exp01.jpg',0)
cv2.imwrite('demos.jpg',image)
```

### Output

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/50823699-726f-481f-a342-f4faf622bfdd)


## Program:

### (iii) Shape of the Image

```py
#Shape of the Image
import cv2
image=cv2.imread('exp01.jpg',1)
print(image.shape)
```


### Output

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/12300246-2a74-4f82-985e-d4913c03cc9e)



## Program:

### (iv) Access rows and columns
```py
#Access rows and columns
import random
import cv2
image=cv2.imread('exp01.jpg',1)
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

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/54eed420-6991-4053-8e0b-9668ecaaf426)



## Program:

### (v) Cut and paste portion of image
```py
#Cut and paste portion of image
import cv2
image=cv2.imread('exp01.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output
![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/801475e1-e380-4a5c-a222-4c734b9748a4)



## Program:

### (vi) BGR and RGB to HSV and GRAY
```py
#BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('exp01.jpg',1)
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

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/3f327aec-7928-422e-96a1-ccddf3f947cd)


### Output

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/feb7623b-5052-4ae2-8bac-5a30f82f1986)


## Program:

### (vii) HSV to RGB and BGR

```py
#HSV to RGB and BGR
import cv2
img = cv2.imread('exp01.jpg')
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

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/6926a20e-6bce-4d33-83d7-72aaf2737dc0)


### Output
![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/dbb9741c-facd-4072-b8fc-2a01fb8b0228)




## Program:

### (viii) RGB and BGR to YCrCb
```py

#RGB and BGR to YCrCb
import cv2
img = cv2.imread('exp01.jpg')
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

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/a4cb82a1-1e21-4606-a297-81a6e3907d82)



## Program:

### (ix) Split and merge RGB Image
```py
#Split and merge RGB Image
import cv2
img = cv2.imread('exp01.jpg',1)
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
![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/bdafcf3b-b115-45a1-ba1c-4f02c221f301)



#### Merged RGB

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/10cca0ef-3945-456f-b602-46d1eba8529d)



## Program:

### (x) Split and merge HSV Image
```py
#Split and merge HSV Image
import cv2
img = cv2.imread("exp01.jpg",1)
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


![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/f588dc3c-45e7-4bfc-9511-504f5a8b191d)



### Splitted

![image](https://github.com/swedha333/COLOR_CONVERSIONS_OF-IMAGE/assets/119477784/b914ae8e-255d-46e5-934c-aaa45e87ce97)



## Result:
#### Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
