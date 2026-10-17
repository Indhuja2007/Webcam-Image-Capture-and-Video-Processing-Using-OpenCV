# Image Capture and Video Process
---

## Aim

To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:

1. Write the frame as a JPG file  
2. Display the video  
3. Display the video by resizing the window  
4. Rotate and display the video  

---

## 🛠️ Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  

---

## ⚙️ Algorithm

### Step 1:
Import the required libraries and initialize the webcam using `cv2.VideoCapture()`.

### Step 2:
Capture frames continuously from the webcam.

### Step 3:
Save a frame as a JPG image using `cv2.imwrite()`.

### Step 4:
Display the live video stream using `cv2.imshow()`.

### Step 5:
Resize the frame and rotate it using OpenCV functions, then display the processed frames.

---

## 💻 Program

### Developed By:
**Name: INDHUJA.K** 

### Register No: 21225040133

```
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

```
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

```
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


---

## Output

### i) Write the frame as JPG image

<img width="360" height="457" alt="image" src="https://github.com/user-attachments/assets/d7f8942a-4fb9-4973-9b27-f56ba6c720d5" />



### ii) Display the video
Live webcam video is displayed
<img width="435" height="418" alt="image" src="https://github.com/user-attachments/assets/c87ba365-654b-4290-aeff-556d5784a923" />


### iii) Display the video by resizing the window
Video is shown in resized resolution (640 × 480)
<img width="142" height="432" alt="image" src="https://github.com/user-attachments/assets/7ef39057-e734-4c61-9b2f-f624acb6e6ef" />


### iv) Rotate and display the video
Video is displayed after rotation (90° clockwise)
<img width="308" height="297" alt="image" src="https://github.com/user-attachments/assets/d007acc7-3967-4da7-88bc-736edcbef4d7" />


---

## Result

Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.
