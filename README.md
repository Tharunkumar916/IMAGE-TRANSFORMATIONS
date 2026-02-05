# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules

### Step2:

Choose an image and save it as filename.jpg

### Step3:

Use imread to read the image

### Step4:

Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:

Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:

Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:

Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:

Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:

Crop the image to remove unwanted areas from an image

### Step10:

Use cv2.imshow to show the image

### Step11:

End the program

## Program:
```python
Developed By:Tharun Kumar V
Register Number: 212224240173
i)Image Translation
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("dipt ex img.jpg")
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")  
plt.axis('off')
#image translation
tx, ty = 100, 50  
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])  
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))  
plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))  
plt.title("Translated Image")  
plt.axis('off')


ii) Image Scaling
#scaled image
fx, fy = 5.0, 2.0 
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)
plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image")  
plt.axis('off')



iii)Image shearing
#image shearing
shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB)) 
plt.title("Sheared Image") 
plt.axis('off')



iv)Image Reflection
#Reflected image
reflected_image = cv2.flip(image, 2)  
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))  
plt.title("Reflected Image") 
plt.axis('off')





v)Image Rotation
# Rotated Image
(height, width) = image.shape[:2] 
angle = 60 
center = (width // 2, height // 2) 
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)  
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image") 
plt.axis('off')




vi)Image Cropping
# cropped image
x, y, w, h = 100, 100, 200, 150  
cropped_image = image[y:y+h, x:x+w]
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image") 
plt.axis('off')





```
## Output:
### i)Image Translation
<img width="676" height="501" alt="Screenshot 2026-02-05 142211" src="https://github.com/user-attachments/assets/1537cdd4-3661-4dec-9ca0-9556b9833546" />


<br>


### ii) Image Scaling
<img width="728" height="259" alt="Screenshot 2026-02-05 142259" src="https://github.com/user-attachments/assets/293ccd88-a333-4319-aaeb-ef587ea39f66" />


<br>



### iii)Image shearing
<img width="744" height="509" alt="Screenshot 2026-02-05 142411" src="https://github.com/user-attachments/assets/8037bfa9-2e03-4faa-b6a0-18d7e2ad9ac8" />

<br>


### iv)Image Reflection
<img width="759" height="498" alt="Screenshot 2026-02-05 142504" src="https://github.com/user-attachments/assets/e5ce0485-8788-4207-b66e-3aac5f82b14f" />

<br>




### v)Image Rotation
<img width="758" height="503" alt="Screenshot 2026-02-05 142548" src="https://github.com/user-attachments/assets/323b7159-71be-49d8-adf1-67dfbf196ea4" />

<br>



### vi)Image Cropping
<img width="678" height="551" alt="Screenshot 2026-02-05 142625" src="https://github.com/user-attachments/assets/e6534dcd-4495-46b2-b58e-330bc0b6dbeb" />

<br>





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
