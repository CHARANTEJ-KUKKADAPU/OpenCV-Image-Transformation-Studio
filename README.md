# Image Handling and Pixel Transformations using OpenCV

This project demonstrates fundamental image processing operations using **Python**, **OpenCV**, **NumPy**, and **Matplotlib**. It covers grayscale conversion, image cropping, resizing, flipping, brightness and contrast adjustment, text annotation, and shape drawing on images.

---

## 📌 Project Overview

The objective of this project is to perform essential image manipulation and pixel transformation tasks commonly used in Computer Vision and Digital Image Processing.

The notebook includes:

* Reading grayscale and color images
* Extracting image dimensions and channels
* Saving images in different formats
* Cropping objects from images
* Resizing and flipping images
* Adding text annotations
* Drawing rectangles on images
* Brightness enhancement and reduction
* Contrast adjustment

This project helps build a strong foundation for advanced OpenCV applications.

---

## 🛠 Technologies Used

* **Python**
* **OpenCV (cv2)**
* **NumPy**
* **Matplotlib**
* **Jupyter Notebook**

---

## 📂 Project Files

```text
├── image_handling.ipynb
├── Eagle_in_Flight.jpg
├── Apollo-11-launch.jpg
├── boy.jpg
├── output.png
└── README.md
```

---

##Operations Performed

### 1. Grayscale Image Reading

```python
img_gray = cv2.imread('Eagle_in_Flight.jpg', cv2.IMREAD_GRAYSCALE)
```

The eagle image is loaded in grayscale format for basic pixel analysis.

<img width="768" height="600" alt="eagle" src="https://github.com/user-attachments/assets/a4ea3337-b0e9-4d96-a549-0ded37e50e46" />

---

### 2. Image Dimensions and Channels

```python
h, w = img_gray.shape
```

Displays width, height, and number of channels in the image.

---

### 3. Displaying Image using Matplotlib

```python
plt.imshow(img_gray, cmap='gray')
```

Used to visualize grayscale and color images.

---

### 4. Saving Image as PNG

```python
cv2.imwrite('eagle.png', img_gray)
```

Converts and saves the grayscale image in PNG format.

---

### 5. Color Image Conversion

```python
real_color = cv2.cvtColor(real_color, cv2.COLOR_BGR2RGB)
```

Converts OpenCV BGR format into RGB for correct display.
<img width="679" height="561" alt="image" src="https://github.com/user-attachments/assets/fe3f9ed9-f470-4972-8d06-4b7fac397949" />

---

### 6. Cropping the Eagle Object

```python
cropped = img_rgb[20:420, 210:540]
```

Extracts the eagle from the original image.
<img width="480" height="545" alt="image" src="https://github.com/user-attachments/assets/2fbf32fc-243f-4759-a3cc-e7595fde680a" />

---

### 7. Resize Image by 2x

```python
resized = cv2.resize(cropped, None, fx=2, fy=2)
```

Enlarges the cropped eagle image.
<img width="411" height="518" alt="image" src="https://github.com/user-attachments/assets/68e116a5-68b3-4363-aa7a-e1256a7ca830" />

---

### 8. Horizontal Flip

```python
flipped = cv2.flip(resized, 1)
```

Creates a mirror version of the eagle image.
<img width="635" height="524" alt="image" src="https://github.com/user-attachments/assets/a839fa23-9560-4ea2-840f-c47c6376fd4b" />

---

### 9. Apollo 11 Image Annotation

```python
cv2.putText()
cv2.rectangle()
```

Adds launch information text and a magenta rectangle around the rocket and launch tower.
<img width="629" height="402" alt="image" src="https://github.com/user-attachments/assets/018d75c1-e840-42c6-a1cc-ddaa9e3a1f78" />

---

### 10. Brightness Adjustment

```python
img_brighter = cv2.add(img, matrix)
img_darker = cv2.subtract(img, matrix)
```

Creates brighter and darker versions of the image.
<img width="1365" height="368" alt="image" src="https://github.com/user-attachments/assets/f75c1c23-26ff-4a12-b677-ae8ca7c45f04" />

---

### 11. Contrast Adjustment

```python
img_higher = cv2.convertScaleAbs(img, alpha=1.2, beta=0)
```

Improves image contrast using scaling.
<img width="1357" height="363" alt="image" src="https://github.com/user-attachments/assets/80556793-72b8-4e35-80ef-40a8232211fb" />

---

##  Final Result

This project successfully demonstrates multiple image handling operations and pixel transformations using OpenCV.



