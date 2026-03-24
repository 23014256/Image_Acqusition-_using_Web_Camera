# Image_Acqusition-_using_Web_Camera


## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.


## Program Developed By:
- **Name:** Suman G 
- **Register Number:**  212223240163

## i) Write the frame as JPG file

```PYTHON
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
captured_image = cv2.imread('captured_frame.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()

```


## ii) Display the video

```PYTHON
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```


## iii) Display the video by resizing the window

```PYTHON

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
  

```


## iv) Rotate and display the video

```PYTHON
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release() 
```

## Output

### i) Write the frame as JPG image
</br>

<img width="695" height="512" alt="image" src="https://github.com/user-attachments/assets/4611550a-b5c3-4e70-8d9f-5160989fb50f" />

</br>


### ii) Display the video
</br>
<img width="655" height="483" alt="image" src="https://github.com/user-attachments/assets/832bbb70-8fb3-4d37-8b9b-78b09e797519" />

</br>


### iii) Display the video by resizing the window
</br>
<img width="396" height="492" alt="image" src="https://github.com/user-attachments/assets/b7c26593-7967-43d0-967f-5205471e247a" />

</br>



### iv) Rotate and display the video
</br>
<img width="445" height="492" alt="image" src="https://github.com/user-attachments/assets/b4027beb-5521-4764-aaa1-ff3066495eec" />

</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
