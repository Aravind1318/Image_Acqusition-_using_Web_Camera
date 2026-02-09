
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
<br>

### Step 2:
<br>

### Step 3:
<br>

### Step 4:
<br>

### Step 5:
<br>

## Program:
``` Python
### Developed By: ARAVIND P
### Register No: 212224240015

## i) Write the frame as JPG file
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


## ii) Display the video
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

## iii) Display the video by resizing the window
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




## iv) Rotate and display the video
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
<img width="856" height="713" alt="image" src="https://github.com/user-attachments/assets/551f3ed8-faf2-40fd-82d5-f01e787c6790" />

### ii) Display the video
<img width="840" height="662" alt="image" src="https://github.com/user-attachments/assets/ebd6644a-a821-4018-858b-433a3c4b06a6" />

### iii) Display the video by resizing the window
<img width="471" height="635" alt="image" src="https://github.com/user-attachments/assets/6e5cc4da-b3ca-44d9-ad53-d48b7ae44109" />

### iv) Rotate and display the video
<img width="434" height="650" alt="image" src="https://github.com/user-attachments/assets/8db128f5-4d3e-45d2-b89f-76cb9b89c7c6" />

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
