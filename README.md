# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1
Import the necessary modules.
</br> 

### Step 2
For performing smoothing operation on a image.
 1) Average Filter
 ```
 avg_kernel=np.ones((13,13),np.float32)/169
 average_filter_image=cv2.filter2D(image,-1,avg_kernel)
 ```
 2) Weighted Average Filter
 ```
 wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
 wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
 ```
 3) Gaussian Blur
 ```
 gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
 ```
 4) Median Blur
 ```
 median_blur=cv2.medianBlur(image,11)
 ```
</br> 

### Step 3
For performing sharpening on a image.
 1) Laplacian Kernel
 ```
 lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
 lap_image=cv2.filter2D(image,-1,lap_kernel)
 ```
 2) Laplacian Operator
 ```
 Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
 ```
</br> 

### Step 4
Display all the images with their respective filters.
</br> 


## Program:
```
### Developed By   : Srinivasan S
### Register Number: 212220230048
```
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
weight_average_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weight_average_filter_image=cv2.filter2D(image,-1,weight_average_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[30:200,50:200])
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()
```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
laplacian_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
laplacian_image=cv2.filter2D(image,-1,laplacian_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(laplacian_image)
plt.show()
```
ii) Using Laplacian Operator
```Python
Laplacian_sharp=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Operator Filter image')
plt.imshow(Laplacian_sharp)
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
