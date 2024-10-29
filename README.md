# Basic-image-manipulations

# 1
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


# 2

### Reading the Image: Reads 'Emerald_Lakes_New_Zealand.jpg' as a color image using cv2.imread.
### Printing Image Shape: Prints the shape of the original color image.
### Converting to Grayscale: Converts the color image to grayscale with cv2.cvtColor.
### Resizing: Scales up the cropped region by a factor of 2x.
### Printing Grayscale Shape: Prints the shape of the grayscale image.
### Displaying the Grayscale Image: Displays the grayscale image using matplotlib.pyplot.imshow.

## Code:
```
import cv2
import matplotlib.pyplot as plt

# Step 1: Read the saved image ('Emerald_Lakes_New_Zealand.jpg') as a color image.
image = cv2.imread('Emerald_Lakes_New_Zealand.jpg', cv2.IMREAD_COLOR)

# Step 2: Print the image shape.
print("Color image shape:", image.shape)

# Step 3: Convert the image to grayscale using cv2.cvtColor().
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Step 4: Print the grayscale image shape.
print("Grayscale image shape:", gray_image.shape)

# Step 5: Display the grayscale image using matplotlib imshow.
plt.figure(figsize=[10, 10])
plt.imshow(gray_image, cmap='gray')  # Displaying in grayscale
plt.show()
```
## Output:
<img width="844" alt="Screenshot 2024-10-29 at 11 51 42 AM" src="https://github.com/user-attachments/assets/0562f4cb-3470-441a-9662-e91723e27e02">



# 3

### Reads 'Apollo-11-launch.jpg' as a grayscale image.
### Printing Dimensions: Retrieves and prints the width and height of the image.
### Displaying the Image: Shows the grayscale image using matplotlib.pyplot.imshow.
### Saving the Image: Saves the grayscale image as 'Apollo-11-launch.png' in PNG format.


## Code:
```
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('jjj.jpeg', cv2.IMREAD_GRAYSCALE)


plt.imshow(image, cmap='gray')
height, width = image.shape
print("Width:", width)
print("Height:", height)

plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('off')
plt.show()


cv2.imwrite('apollo.png', image)
```

## Output
<img width="652" alt="Screenshot 2024-10-29 at 11 57 20 AM" src="https://github.com/user-attachments/assets/b98cd71a-50e5-4f67-87ff-8a71bcf00ce8">


# 3

### Reading the Image: Reads 'Apollo-11-launch.jpg' in color.
### Adding Text: Places the text "Apollo 11 Saturn V Launch, July 16, 1969" at the bottom center of the image.
### Drawing the Rectangle: Draws a magenta rectangle around the specified coordinates, intended to outline the launch tower and rocket.
### Displaying the Image: Shows the annotated image using matplotlib.

## Code:
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("jjj.jpeg")
fig, ax = plt.subplots()
ax.imshow(image)
ax.set_xticks(range(0, image.shape[1], 100))
ax.set_yticks(range(0, image.shape[0], 100))
plt.show()
image = cv2.imread("jjj.jpeg")
x, y = 500, 50
width = 200
height = 600
cv2.rectangle(image, (x, y), (x + width, y + height), (0, 0, 255), 3)
fig, ax = plt.subplots()
ax.imshow(image)
ax.set_xticks(range(0, image.shape[1], 100))
ax.set_yticks(range(0, image.shape[0], 100))
plt.show()
```
## Output:
<img width="609" alt="Screenshot 2024-10-29 at 11 58 58 AM" src="https://github.com/user-attachments/assets/4dbbcd3f-13ba-4136-9ddc-cf94ed78e53e">


