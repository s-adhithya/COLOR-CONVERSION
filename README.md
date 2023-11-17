# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import opencv.

### Step2:
Read the original Image.

### Step3:
Store the required conversion of the image in a variable.

### Step4:
Show the image stored in the given variable.

### Step5:
Destroy all the windows and end the program.

## Program:

Developed By: Adhithya.S

Register Number: 212222240003

i) Convert BGR and RGB to HSV and GRAY
```python
import cv2

flower_image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', flower_image)

hsv_bgr_image = cv2.cvtColor(flower_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_bgr_image)

hsv_rgb_image = cv2.cvtColor(flower_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_rgb_image)

gray_bgr_image = cv2.cvtColor(flower_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_bgr_image)

gray_rgb_image = cv2.cvtColor(flower_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_rgb_image)

cv2.waitKey(0)
cv2.destroyAllWindows()

```


# ii)Convert HSV to RGB and BGR
```
import cv2

flower_hsv_image = cv2.imread('flower.jpg')
cv2.imshow('Original HSV Image', flower_hsv_image)

rgb_image = cv2.cvtColor(flower_hsv_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB', rgb_image)

bgr_image = cv2.cvtColor(flower_hsv_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR', bgr_image)

cv2.waitKey(0)
cv2.destroyAllWindows()
```



# iii)Convert RGB and BGR to YCrCb
```
import cv2
image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)
ycrcb_image_rgb = cv2.cvtColor(image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB to YCrCb', ycrcb_image_rgb)
ycrcb_image_bgr = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR to YCrCb', ycrcb_image_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


# iv)Split and Merge RGB Image
```
import cv2
image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel', blue)
cv2.imshow('G-Channel', green)
cv2.imshow('R-Channel', red)
merged_bgr = cv2.merge((blue, green, red))
cv2.imshow('Merged BGR Image', merged_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# v) Split and merge HSV Image
```
import cv2

image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)

hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)

cv2.imshow('Hue - Image', h)
cv2.imshow('Saturation - Image', s)
cv2.imshow('Value - Image', v)

merged_hsv = cv2.merge((h, s, v))
cv2.imshow('Merged HSV Image', merged_hsv)

cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:
### i)BGR and RGB to HSV and GRAY
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/ef2a5399-c9fc-4e75-a5c1-772ff82c3c06)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/f1047203-0aa7-4a7e-af13-c7369a4a5068)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/7738d1cf-a585-47a8-b59a-74c82b4ba0ba)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/88470509-2c14-4264-a8fe-91420309f703)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/96342665-8f0d-4955-a788-2005a57d74b3)


### ii) HSV to RGB and BGR
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/c56fc05f-41dd-4f88-8585-e1ff8b80ca42)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/4a252678-5832-47a9-9bd8-a494ed967aa7)


### iii) RGB and BGR to YCrCb
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/3f6776e2-df05-40e1-b63d-9dc1b79c275e)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/d176927a-3138-410c-b3ed-a233c9820280)


### iv) Split and merge RGB Image
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/053cee06-0c55-474a-91dd-26bd8a6a908e)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/ba2be870-780d-4549-a875-2a5a354af030)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/a15e72ef-25e2-41d5-90ae-a239ebcd04a3)


### v) Split and merge HSV Image
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/f3b4f07e-5104-416d-b6cb-f06d691c90f4)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/f1459838-5cc3-4756-bf2d-cc6adadbb08e)
![image](https://github.com/s-adhithya/COLOR-CONVERSION/assets/113497423/64b8bf0e-587c-43e3-a807-3fc51e139d26)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
