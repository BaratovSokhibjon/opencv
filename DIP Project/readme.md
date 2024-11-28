## CSRT Tracker
## How does it track?

### Spatial reliability maps
- The CSRT creates reliability maps according to the easy-to-spot or highlighted part of the object (it has its own detection)
It breaks the object into small regions and then checks how reliable each part is
Instead of relying on the whole object, the CSRT will keep focusing on reliable parts (faster, better when other parts are blurry, change color)
The CSRT keeps checking which parts of the object is reliable effectively keeping track of the object even when the object changes its  direction/trajectory

### Channel filtering
- It is like dividing the image into several channels or layers to determine which one is giving the most valueable information for detecting the object. And the helpful layers are given more attention just like focusing on the outline of the car rather than its reflection in a shiny window

### Filter optimization 
- this part of the CSRT focuses on magnifying and focusing on the important parts of the object so that the object is easier to find.

### Feature Extraction
- HOG and Color names: Histogram of Oriented Gradients helps to capture the shape and edges of the object, like detecting the outline of the object. Color names help to track the colors of the object so it can detect better.

### Search area expansion
- when the object moves fast for the CSRT to detect, CSRT will increase the area it is looking by zooming out to find where the object went.

### Regularization and Localizatrion
- to avoid getting stuck, CSRT doesn't keep focusing only in tiny details of the object and balances the focus across the object which is called regularization.
- to find exact position of the object, csrt uses all the clues like edges, colors, shapes and predicts where the object most likely to be in the next frame