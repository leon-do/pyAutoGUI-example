```python

# clicking
import pyautogui
# get image
from PIL import ImageGrab, ImageOps
# convert image to number
import numpy
# pause
import time


def image_sum(x1: float, y1: float, x2: float, y2: float):
    image = ImageGrab.grab((x1, y1, x2, y2))
    grey_image = ImageOps.grayscale(image)
    grey_image_array = numpy.array(grey_image.getcolors())
    grey_image_sum = grey_image_array.sum()
    return grey_image_sum


print(image_sum(400, 400, 500, 500))

time.sleep(1)

# https://pyautogui.readthedocs.io/en/latest/cheatsheet.html
pyautogui.click(1285, 405)


```
