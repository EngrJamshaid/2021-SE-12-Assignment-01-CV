# 2021-SE-12-Assignment-01-CV

# Hybrid Image Creation in Google Colab

## Overview
This Assignment demonstrates how to create *hybrid images* by combining the low-frequency components of one image with the high-frequency components of another. The result is a hybrid image that changes appearance based on the viewing distance:
- From a distance: The low-frequency image is visible.
- Up close: The high-frequency image dominates.

This project uses Python and OpenCV, and it is designed to run in *Google Colab*.

---

## Features
- Upload two images directly through Google Colab.
- Automatically aligns and resizes images to match dimensions.
- Combines frequency components to generate a unique hybrid image.
- Displays and saves the resulting hybrid image.

---

## How It Works
### 1. *Image Preparation*
- The user uploads two images:
  - Image 1*: Treated as the low-frequency component.
  - ![download](https://github.com/user-attachments/assets/3b676c2e-f455-4293-9eef-c9c684183d1e)

  - Image 2*: Treated as the high-frequency component.
  - ![download (1)](https://github.com/user-attachments/assets/f1822c48-1127-48ee-b42d-ad7907116434)

  
### 2. *Frequency Processing*
- *Low-Frequency Extraction*: 
  - A Gaussian blur is applied to Image 1 to smooth out fine details and retain the overall structure.
- *High-Frequency Extraction*:
  - The blurred version of Image 2 is subtracted from itself to isolate sharp edges and fine details.

### 3. *Hybrid Image Creation*
- The low-frequency image from Image 1 is added to the high-frequency image from Image 2, creating the hybrid image.

### 4. *Output*
- The hybrid image is displayed alongside the original input images.
- It can also be saved as a file (hybrid_image.jpg).


<img width="730" alt="hybrid image" src="https://github.com/user-attachments/assets/2a8d5ca9-d903-4a26-b95f-dac814e3ed12">



## Google Colab Setup
Follow these steps to run the code in Google Colab:
1. Open Google Colab: [Google Colab](https://colab.research.google.com).
2. Copy and paste the Python code into a new notebook.
3. Run the code cells step by step:
   - Upload two images when prompted.
   - View the hybrid image in the output.

---

## Code Explanation
## Functions:
- **upload_image()**: Allows users to upload images from their local system.
- **create_hybrid_image(image1, image2)**: Processes the two uploaded images to create a hybrid image.

### Key Libraries:
- **OpenCV (cv2): Handles image processing tasks like blurring, resizing, and combining images.
- **NumPy (np): Assists with matrix operations.
- **Matplotlib (plt): Visualizes images directly in the notebook.

---

## Example Workflow
1. *Input Images*:
   - Upload an image of a cat (low-frequency).
   - Upload an image of a dog's face (high-frequency).
   
2. *Output Hybrid Image*:
   - The resulting image will look like a smoothed-out cat from far away and a detailed dog face up close.

---

## Results
The program will display three images:
1. The first image (low-frequency).
2. The second image (high-frequency).
3. The final hybrid image.

---

## File Output
The hybrid image is automatically saved as **hybrid_image.jpg** in the notebook's directory.

---

## Prerequisites
- *Python Libraries*: Ensure OpenCV, NumPy, and Matplotlib are installed (Google Colab has these pre-installed).
- *Images*: Two images to upload for hybrid image creation.

---

## Future Improvements
- Allow users to adjust the frequency blend dynamically.
- Extend support for color images in hybrid creation.
- Add a graphical interface for easier interaction.

