# Basic-image-manipulations

### Reading the Image: The code reads the image in color using cv2.imread.
### Displaying the Image: Displays the original image with matplotlib.pyplot.imshow after adjusting the color channels.
### Cropping the Image: Crops a specific region around the sailboat (replace (x1, y1, x2, y2) with the coordinates for the sailboat).
### Resizing: Scales up the cropped region by a factor of 2x.
### Flipping: Flips the resized image horizontally.
### Displaying the Final Image: Shows the final flipped and resized image.

## Code-
```import cv2
import matplotlib.pyplot as plt

img = cv2.imread('New_Zealand_Boat.jpeg', cv2.IMREAD_COLOR)
plt.figure(figsize=[3, 3])
plt.imshow(img[:, :, ::-1])  
plt.show()

cropped_img = img[200:300, 300:450]

resized_img = cv2.resize(cropped_img, (0, 0), fx=2, fy=2)

flipped_img = cv2.flip(resized_img, 1)


plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1])  
plt.show()
```

### Output:
<img width="708" alt="Screenshot 2024-10-29 at 11 47 24 AM" src="https://github.com/user-attachments/assets/838cb98c-84d5-4a68-9711-db4eb6ee9c83">



