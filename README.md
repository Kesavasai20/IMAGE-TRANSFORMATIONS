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

## Step6:
Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

## Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

## Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

## Step9:
Crop the image to remove unwanted areas from an image

## Step10:
Use cv2.imshow to show the image

## Step11:

End the program

## Program:
```py
'''
Developed By: K KESAVA SAI
Register Number: 212223230105
'''
```
## i) Original Image
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car1.png")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(image)
plt.show()
```

## ii)Image Translation
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car1.png")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[1,0,114],[0,1,-230],[0,0,1]])
translated_image = cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

## iii) Image Scaling
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car1.png")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[2.4,0 ,0],[0,1.9,0],[0,0,1]])
scaled_image = cv2.warpPerspective(image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```

## iv)Image shearing
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car1.png")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0.8 ,0],[0,1,0],[0,0,1]])
M_y = np.float32([[1,0,0],[0.6,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.imshow(sheared_img_yaxis)
plt.show()
```

## v)Image Reflection
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car1.png")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0 ,0],[0,-1,rows],[0,0,1]])
M_y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.imshow(reflected_img_yaxis)
plt.show()
```

## vi)Image Rotation
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car1.png")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
angle = np.radians(10)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```

## vii)Image Cropping
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car1.png")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
cropped_img = image[100:800,20:400]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```

## Output:
### i) Original Image
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/04502686-3682-430b-825b-c12030c6f235)
### ii)Image Translation
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/5e94a31b-9cf9-4225-b32f-a4ebde229724)
### iii) Image Scaling
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/2a48b52d-5a89-4d77-a3c1-a0bcc77e81d3)
### iv)Image shearing
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/b69e5d60-d053-4b3f-bf1f-bcb9f2efebbb)
### v)Image Reflection
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/e02e907f-3a52-418f-aded-b066540f6cd6)
### vi)Image Rotation
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/acd42973-a996-4141-9336-14cffada964a)
### vii)Image Cropping
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/e0bbb36c-95bb-4764-bf86-fac7b0988f0d)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
