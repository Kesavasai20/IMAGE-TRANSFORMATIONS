# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
'''
Developed By: K KESAVA SAI
Register Number: 212223230105
'''
## i) Original Image
```
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
```
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
```
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
```
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
```
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
```
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
```
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
<br>
<br>
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/0602c535-34f2-4d8f-84cf-7e92f5f10589)

<br>
<br>

### ii)Image Translation
<br>
<br>
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/9e325759-8cf9-4130-a7e3-5b2a18b7b2a1)

<br>
<br>

### iii) Image Scaling
<br>
<br>
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/a6056518-7a4e-4619-b38f-0dbde1e2e83b)

<br>
<br>


### iv)Image shearing
<br>
<br>
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/0b3cf633-ca21-44c1-9420-c51e6e26d7aa)

<br>
<br>


### v)Image Reflection
<br>
<br>
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/94bad7b4-e428-444e-9918-5bd5c66f581f)

<br>
<br>



### vi)Image Rotation
<br>
<br>
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/e6d15242-bd39-47e7-bd69-3dc69b2031df)

<br>
<br>



### vii)Image Cropping
<br>
<br>
![image](https://github.com/Kesavasai20/IMAGE-TRANSFORMATIONS/assets/138849303/0a7ced29-91e0-49f1-928c-07a8eb9cd2df)

<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
