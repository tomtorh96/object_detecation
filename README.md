# computer vision project

This project contains two main Jupyter notebooks:

- `dataset.ipynb`: Handles data preparation, extraction, and conversion to COCO format for object detection tasks.
- `training.ipynb`: (Content not shown here, but typically used for model training and evaluation.)

## dataset.ipynb

This notebook performs the following steps:

1. **Environment Setup**

   - Installs required Python packages (e.g., `transformers`).
   - Imports libraries such as PyTorch, NumPy, Matplotlib, PIL, and others.

2. **Google Drive Integration**

   - Mounts Google Drive to access datasets and save outputs (for Colab usage).

3. **Data Extraction**

   - Extracts image data from a ZIP archive stored in Google Drive.

4. **Model Loading**

   - Loads a pre-trained model (`microsoft/Florence-2-large`) and processor from Hugging Face Transformers for image analysis.

5. **Image Processing**

   - Selects a subset of images for processing.
   - Runs object detection on each image using the loaded model.
   - Handles errors gracefully and skips problematic images.

6. **Saving Results**

   - Saves processed data and the list of used images as JSON files to Google Drive.

7. **COCO Format Conversion**
   - Defines a function to convert model outputs and image metadata into the COCO dataset format, with two categories: `human` and `pet`.
   - Saves the final COCO-formatted dataset as a JSON file.

## training.ipynb

This notebook is intended for training machine learning models using the dataset prepared in `dataset.ipynb`. Typical steps may include:

- Loading the COCO-formatted dataset.
- Defining and configuring a neural network model (e.g., using PyTorch).
- Training the model on the dataset.
- Evaluating model performance.
- Saving trained models and results.

## Requirements

- Python 3.7+
- Jupyter Notebook
- PyTorch
- Transformers (specific version: 4.49.0)
- PIL (Pillow)
- tqdm
- Google Colab (for Drive integration, or adapt paths for local use)

## Notes

- Paths and Google Drive mounting are set up for Google Colab. If running locally, adjust file paths and remove Colab-specific code.
- The dataset and outputs are expected to be in specific directories as referenced in the notebooks.

---

For more details, see the code and comments in each notebook.
