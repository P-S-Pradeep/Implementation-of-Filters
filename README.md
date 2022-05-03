# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules.


### Step2
For performing smoothing operation on a image.

Average filter
```
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
Weighted average filter
```
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```
Gaussian Blur
```
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```
Median filter
```
median_blur=cv2.medianBlur(image,11)
```

### Step3
For performing sharpening on a image.
```
Laplacian Kernel
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```
Laplacian Operator
```
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```

### Step4
Display all the images with their respective filters.


Program:

Developed By : Pradeep P S
Register Number: 212220230034

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
plt.imshow(image[70:700,300:700])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[70:700,300:700])
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
</br>![Screenshot (23)](https://user-images.githubusercontent.com/102652887/166447042-17c617d4-bb59-4b51-8964-cedc0ab61f25.png)
</br>
</br>

ii) Using Weighted Averaging Filter
</br>
</br>
</br>![Screenshot (24)](https://user-images.githubusercontent.com/102652887/166447054-e7aa5113-3c70-454c-b635-222272b7b7e0.png)
</br>
</br>

iii) Using Weighted Averaging Filter
</br>
</br>
</br>![Screenshot (25)](https://user-images.githubusercontent.com/102652887/166447068-64b4c9ef-d7d9-42d2-8c3b-751b93be3fc4.png)
</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>![Screenshot (26)](https://user-images.githubusercontent.com/102652887/166447111-229272aa-2a7d-4a56-8bc7-31c20724a820.png)
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br>![Screenshot (27)](https://user-images.githubusercontent.com/102652887/166447117-4f6dc0ae-5e16-4a85-84e2-8e0c317d9d4d.png)
</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
</br>![Screenshot (28)](https://user-images.githubusercontent.com/102652887/166447126-6a02d933-0897-483e-b90b-189720c34617.png)
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
