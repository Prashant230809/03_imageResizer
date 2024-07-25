# Image Resizer Program
This program will help you to resize your program with the help of **opencv-python** module.

1. To able to do that you need to have opencv-python module install. 

    ``pip install opencv-python``

2. Then move your file into the project and set the parametters.
```python
# Configurable Parameters
source = "image.jpg"
destination = "newImage.jpg"
scale_percent = 50
```
3. Then run the following code
```python
import cv2

# Configurable Parameters
source = "image.jpg"
destination = "newImage.jpg"
scale_percent = 50


src = cv2.imread(source, cv2.IMREAD_UNCHANGED)
# cv2.imshow("image", src)

new_width = int(src.shape[1] * scale_percent / 100)
new_height = int(src.shape[0] * scale_percent / 100)


output = cv2.resize(src, (new_width, new_height))

cv2.imwrite(destination, output)
# cv2.waitKey(0)
```
That's all you need to do