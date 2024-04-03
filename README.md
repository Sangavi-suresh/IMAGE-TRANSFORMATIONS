# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Find reflection of image.

### Step6:
Rotate the image.

### Step7:
Crop the image.

### Step8:
Display all the Transformed images.

## Program:
```python
Developed By:  SANGAVI SURESH
Register Number:212222230130
```
i)Image Translation

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(lion_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```
iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
dog_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```


v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(lion_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```

vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
cropped_img=lion_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```


```
## Output:
### i)Image Translation

![312374463-28156dcf-358e-4bc1-8262-8d026159bcc0](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/f0c0177d-48a0-4c35-8986-81d0b2c0ae18)

![312374545-254f434d-3808-4628-8040-7831b9d50803](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/084e98f6-7ac9-496a-81be-8e08721006c8)

### ii) Image Scaling

![312374657-da2728bc-22a4-47a1-b683-d75e0291376c](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/0ef5eb0a-68a8-49c3-bd9b-4043e0c35bab)

![312374933-e7f7463a-3e2d-48ad-8406-b4a831ebdd9a](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/6c6b053e-6f16-4c18-b8ad-94d6dd12e7e1)

### iii)Image shearing

![312375178-5eaf2b39-a0cf-4c85-89ee-7a2928a0fca3](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/eb928870-e125-4477-96b3-63ee63f0d3be)

![312375329-96356b1a-686f-4e7a-8996-45e36e3ae1d9](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/9e97f900-30d7-4408-aa57-06907d7c9adb)

![312375357-7fa18db4-06e2-4471-95aa-7ab174d3b87b](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/a178902a-9362-4a45-b4cd-4d9a3e4ff336)

### iv)Image Reflection

![312375415-3c4971f8-b8a4-406a-ba60-323f93415606](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/62ffae1f-2243-47da-a6ca-701f2cd5f482)

![312375626-93b26f93-cfac-4aa8-9d27-48535c97ec39](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/46bbd06a-ccc8-4075-a636-f5feafcc329f)

![312375836-7b3519cd-4921-4575-8827-6b2ac904188a](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/79585e81-dc47-41ef-8fac-3d11b49cb666)

### v)Image Rotation

![312376505-28d4f6bb-3754-42e7-b083-41dedf08c2dc](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/7fa2fc46-73e5-4a18-ad89-c0650f17df6f)

![312376688-a92d58a5-491a-401d-9a76-e265765116b4](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/761f1fce-62e3-48b0-9dd9-135a3a44ee83)


### vi)Image Cropping

![312376892-b383a754-4e25-44fc-b6f2-f7f3be01cfae](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/39528ccd-4b6a-40f2-b3b3-34cf412ca6bb)

![312376986-ccb76dd9-491b-42d1-88fe-470361a89020](https://github.com/Sangavi-suresh/IMAGE-TRANSFORMATIONS/assets/118541861/938d02a5-ccba-48cc-a5e2-6ea6e0fc34ae)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
