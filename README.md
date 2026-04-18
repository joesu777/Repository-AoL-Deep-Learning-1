# Maritime Small Object Detection using YOLOv8

### notebooks/: Colab notebook containing the full pipeline
### models/: Custom model architecture for the YOLOv8 + CBAM 
### results/: Sample outputs for qualitative comparison across methods
### weights/: Link to pretrained model weights (not including SAHI)


### Running the notebook: 
It is highly recommended to run the notebook in Colab as a built-in environment is already present, 
as well as a built-in GPU. 

If not, run pip install -r requirements.txt locally with the requirements.txt present in this repository for the requirements. 

### Requirements for Running the Code
To run this code, you will need: 
- Kaggle legacy API (kaggle.json file), which must be uploaded at the start to download the dataset
- Potentially rename some of the model paths as they should point to the .pt weights, which are in the Google Drive. 

### Running Inference Only
To run inference only, run all cells that do not include the training mechanism, and do not copy the model resuts to the Drive. In Colab, for install sahi, 
you may need to restart the environment. After restarting, do not rerun the pip installation for sahi, 
and immediately import the library. 

### Notes for Colab Suage
If there is an error regarding a library, most likely a cell that contained an import has not been run. 
For CBAM, this cell is necessary for Colab to recognize it: 

### CBAM Integration
import ultralytics.nn.tasks as tasks
tasks.CBAM = CBAM





