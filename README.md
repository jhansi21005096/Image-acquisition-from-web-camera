# Image-Acquisition-from-Web-Camera
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
<br>Import Open cv Package.

### Step 2:
<br>Capture the video from the WebCamera.

### Step 3:
<br>Write the image to the file.

### Step 4:
<br>Show the image or the Live Camera

### Step 5:
<br>End the program

## Program:
``` Python
### Developed By:K.Jhansi
### Register No:212221230045

## i) Write the frame as JPG file
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('myimage',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()



## ii) Display the video
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('myimage',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()



## iii) Display the video by resizing the window
import numpy as np
import cv2
imgsrc = cv2.VideoCapture(0)
while True:
    src,frame = imgsrc.read()
    width = int(imgsrc.get(3))
    height = int(imgsrc.get(4))
    img = np.zeros(frame.shape,np.uint8)
    Frame = cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2,:width//2] = smaller_frame
    image[height//2:,:width//2] = smaller_frame
    image[:height//2,width//2:] = smaller_frame
    image[height//2:,width//2:] = smaller_frame
    cv2.imshow('frame',image)
    if cv2.waitKey(1) == ord('g'):
           break
imgsrc.release()
cv2.destroyAllWindows()



## iv) Rotate and display the video
import numpy as np
import cv2
imgsrc = cv2.VideoCapture(0)
while True:
    src,frame = imgsrc.read()
    width = int(imgsrc.get(3))
    height = int(imgsrc.get(4))
    img = np.zeros(frame.shape,np.uint8)
    Frame = cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2,:width//2] = smaller_frame
    image[height//2:,:width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[:height//2,width//2:] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:,width//2:] = smaller_frame
    cv2.imshow('frame',image)
    if cv2.waitKey(1) == ord('g'):
           break
imgsrc.release()
cv2.destroyAllWindows()

```
## Output

### i) Write the frame as JPG image
![output](https://github.com/jhansi21005096/Image-acquisition-from-web-camera/blob/main/image.jpeg)


### ii) Display the video

![output](https://github.com/jhansi21005096/Image-acquisition-from-web-camera/blob/main/video.jpeg)

### iii) Display the video by resizing the window
![output](https://github.com/jhansi21005096/Image-acquisition-from-web-camera/blob/main/4pics.jpeg)


### iv) Rotate and display the video
![output](https://github.com/jhansi21005096/Image-acquisition-from-web-camera/blob/main/rotate.jpeg)





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
