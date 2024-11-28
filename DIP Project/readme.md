# Object Tracking Algorithms

## CSRT Tracker
CSRT Tracker uses spatial reliability maps for adjusting the filter support to the part of the selected region from the frame for tracking. This gives it the ability to increase the search area and track non-rectangular objects. Reliability indices reflect the quality of the studied filters by channel and are used as weights for localization. Using HoGs and ColorNames as feature sets, the algorithm performs relatively well.

### Pros:
- Comparatively better accuracy than other algorithms.
- Resistant to overlapping by other objects.

### Cons:
- Low speed.
- Unstable operation when the object is lost.

---

## MOSSE Tracker
MOSSE Tracker is based on the calculation of adaptive correlations in Fourier space. The filter minimizes the sum of squared errors between the actual correlation output and the predicted correlation output. This tracker is robust to changes in lighting, scale, pose, and non-rigid deformations of the object.

### Pros:
- Very high tracking speed.
- More successful in continuing tracking the object even if it was lost.

### Cons:
- High likelihood of continuing tracking if the subject is lost and does not reappear in the frame.

---

## GOTURN (Generic Object Tracking Using Regression Network) Tracker
GOTURN Tracker is an “offline” tracker since it uses a deep convolutional neural network. Two images are fed into the network: the “previous” and the “current.” In the “previous” image, the position of the object is known, while in the “current” image, the position of the object must be predicted. Both images are passed through a convolutional neural network, which outputs a set of 4 points representing the coordinates of the predicted bounding box containing the object. As this algorithm is based on a neural network, the user needs to download and specify the model and weight files for tracking.

### Pros:
- Good resistance to noise and obstructions.

### Cons:
- The accuracy of tracking depends on the data used to train the model, which may result in poor tracking for certain objects.
- Struggles with high-speed objects, often losing the object and shifting to another.

---

This document compares three popular object tracking algorithms (CSRT, MOSSE, and GOTURN) based on their functionality, advantages, and disadvantages.
