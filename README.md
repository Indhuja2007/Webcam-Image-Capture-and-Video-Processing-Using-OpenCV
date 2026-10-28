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

## 💻 Program And Output

### Developed By:
**Name: INDHUJA.K** 

### Register No: 21225040133


### i) Write the frame as JPG image
```
import cv2

cap = cv2.VideoCapture(0)

ret, frame = cap.read()

if ret:
    cv2.imwrite("pyramit.jpeg", frame)
    cv2.imshow("Captured Image", frame)
    cv2.waitKey(0)

cap.release()
cv2.destroyAllWindows()
```
<img width="787" height="627" alt="Screenshot 2026-10-28 094713" src="https://github.com/user-attachments/assets/b9ae66cf-b0d5-47c5-94cc-9811b3c89de3" />


### ii) Display the video

```
import cv2

cap = cv2.VideoCapture(0)

while True:
    ret, frame = cap.read()

    if not ret:
        break

    cv2.imshow("Live Video", frame)

    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```
<img width="800" height="636" alt="image" src="https://github.com/user-attachments/assets/be245195-f07b-4e7a-bd2f-03ab1735cc26" />


### iii) Display the video by resizing the window
```
import cv2

cap = cv2.VideoCapture(0)

while True:
    ret, frame = cap.read()

    if not ret:
        break

    resized = cv2.resize(frame, (320, 240))

    cv2.imshow("Resized Video", resized)

    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

<img width="395" height="332" alt="image" src="https://github.com/user-attachments/assets/5440c694-21b0-4e3d-b8e2-3eb13a90a385" />


### iv) Rotate and display the video
```
import cv2

cap = cv2.VideoCapture(0)

while True:
    ret, frame = cap.read()

    if not ret:
        break

    rotated = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)

    cv2.imshow("Rotated Video", rotated)

    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```


<img width="588" height="827" alt="image" src="https://github.com/user-attachments/assets/091daced-4992-4c96-a233-5491acf29083" />

---

## Result

Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.
