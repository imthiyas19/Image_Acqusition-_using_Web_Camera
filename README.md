# Image_Acqusition-_using_Web_Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera

### Step 2:
Use cv2.imread to read the video or image

### Step 3:
Use cv2.imwrite to save the image

### Step 4:
Use cv2.imshow to show the video

### Step 5:
End the program and close the output video window by pressing 'q

## Program:
``` Python
### Developed By:MOHAMMED IMTHIYAS.M
### Register No:212222230083
```
## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("abishek.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```




## ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('lion',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```




## iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230004_abishek',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```





## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230004_abishek',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```










## Output

### i) Write the frame as JPG image


![307216568-4fce0f33-4d19-4618-926c-d864eaff0b90](https://github.com/imthiyas19/Image_Acqusition-_using_Web_Camera/assets/120353416/35887ac6-f84d-448c-806c-0b66ea5a4ad1)


### ii) Display the video





![307216833-27ebe1ee-c2f9-4174-9d8e-68e4db94b721](https://github.com/imthiyas19/Image_Acqusition-_using_Web_Camera/assets/120353416/bd43715c-dbfa-4c21-87f9-16a088b05fec)





### iii) Display the video by resizing the window






![307216896-a7826f74-2921-47a7-8fb7-ee4bb6e2e1fd](https://github.com/imthiyas19/Image_Acqusition-_using_Web_Camera/assets/120353416/5aa81ee7-503f-4646-83de-f0465c5de834)





### iv) Rotate and display the video






![307216950-d16972f4-c034-442e-af54-4371cdbe825d](https://github.com/imthiyas19/Image_Acqusition-_using_Web_Camera/assets/120353416/f147a68a-d22c-4a5c-b0f8-28cd0159b62d)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.
