# Sunspot Detection using CNN

This project explores sunspot detection by gathering sunspot images, preprocessing them, and training a Convolutional Neural Network (CNN) to analyze and predict sunspot patterns. 

## Project Structure

1. **Data Collection**: 
   - Fetches sunspot data from NASA's **SOHO (Solar and Heliospheric Observatory)** for dates with 0, 4, and 15 sunspots.
   - Uses `asyncio` and `aiohttp` to download images efficiently and stores them by category in a directory.

2. **Image Preprocessing**:
   - Images are resized to fit TensorFlow requirements.
   - Data generators from `tensorflow.keras.preprocessing.image` are used to normalize pixel values and prepare batches for training.

3. **CNN Architecture and Training**:
   - A CNN model is built using Keras with several convolutional, max-pooling, and dropout layers.
   - Includes specific configurations for regularization and dropout to minimize overfitting.
   - Trains using the **Adam optimizer** with a custom learning rate and **early stopping** to improve convergence.

4. **Model Evaluation**:
   - Plots training loss over epochs to evaluate learning progress.
   - Uses **LIME** (Local Interpretable Model-agnostic Explanations) for interpretability, helping visualize the CNN's decision-making process.

## Files and Folders

- **training_images_x**: Contains categorized images used for training the model.
- **CNN Model**: Model architecture and training functions for sunspot detection.

## Setup and Execution

### Prerequisites

- Python 3.10
- Libraries: `tensorflow`, `keras`, `pandas`, `aiohttp`, `asyncio`, `BeautifulSoup`, `html5lib`, `urllib`, `nest_asyncio`, `LIME`

### Run the Notebook

1. **Install dependencies**:
   ```bash
   pip install tensorflow keras pandas aiohttp beautifulsoup4 html5lib urllib3 nest_asyncio lime
   ```

2. **Execute Cells**: Run cells sequentially for the complete process:
   - Data collection and download of sunspot images.
   - Preprocess the downloaded images.
   - Train the CNN model with the preprocessed data.

## Model Training

- Uses images with different sunspot counts to train the CNN.
- Early stopping and learning rate adjustment are applied for efficiency.

## Results and Analysis

- The model’s performance and loss function are plotted.
- **LIME** visualizations provide insights into model predictions for each class.
