# Task 13: Edges and Corner Detection

## Objective
Detect edges and corners in pre-stored images.

## Theory
Edge detection is a fundamental task in image processing used to identify object boundaries. In this project, we used the **Sobel operator** to generate ground truth edge maps and trained a **U-Net model**—a popular convolutional neural network architecture for image segmentation—to learn edge features from grayscale images.

---

## PART 1: Model Building in Jupyter Notebook (VS Code)

### Step 1:
Open VS Code → File → New File

### Step 2:
Choose `Jupyter Notebook`.

### Step 3:
Save the notebook as `edge-corner-detection.ipynb`.

### Step 4:
Import required libraries:
- `cv2` for image processing
- `tensorflow` for model creation
- `sklearn` for data splitting
- `matplotlib` for plotting

> ⚠️ Make sure to install libraries using pip (e.g., `pip install numpy`)

### Step 5:
Select the Python kernel:
- Go to **Python Environments**
- Choose your Python version (e.g., 3.12.3)
- Install any additional requirements if prompted.

### Step 6:
Run the first cell using `Shift+Enter`.

### Step 7:
Download the **Fruits image dataset** from Kaggle.
- Extract the zip
- Dataset contains separate folders for training and testing.

### Step 8:
**Load and Preprocess Images**
- Read images in grayscale
- Resize and normalize them

### Step 9:
Generate edge maps using the **Sobel operator**.

### Step 10:
Perform **train-test split**.

### Step 11:
Define **Dice Loss** function.

### Step 12:
Define the **U-Net model**.

> 💡 Enter the train image folder path based on your system.

### Step 13:
Compile the model.

### Step 14:
Train the model.

### Step 15:
Make predictions on test data.

### Step 16:
Visualize the results.

### Step 17:
Display the output.

### Step 18:
Convert the model to **TFLite** format.

> 💡 Save the `.h5` and `.tflite` models to appropriate paths on your system.

---

## PART 2: Hardware Integration via ST Edge AI Developer Cloud

### Step 1: Sign In
- Visit: [ST Edge AI Developer Cloud](https://www.st.com/en/embedded-software/st-edge-ai-developer-cloud.html)
- Sign in or create an ST account.

### Step 2:
Select your model and click **Start**.

### Step 3:
Select platform → **STM32 MCU with Neural-ART™**.

### Step 4:
Perform optional **Quantization**.

### Step 5:
Click **Optimize**.

### Step 6:
Run **Benchmark** after optimization.

### Step 7:
View **Benchmark Results**.

### Step 8:
Click **Generate**:
- Select **CPU**
- Select **Board**
- Download the STM32CubeIDE Project

### Step 9:
Open the downloaded project in **STM32CubeIDE**.
> ⚠️ Make sure your IDE version matches or exceeds the required version mentioned.

---

## Conclusion
We successfully trained a **U-Net model** to detect edges in grayscale images using **Sobel-generated edge maps**. Though the initial accuracy was ~30%, the model and preprocessing steps lay a solid foundation for future improvement through:
- Hyperparameter tuning
- Data augmentation
- Model enhancements
