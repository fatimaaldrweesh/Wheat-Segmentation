![image](https://github.com/fatimaaldrweesh/Wheat-Segmentation/assets/63796712/13cb82c2-81a5-4696-873f-f88c2a3a6c4c)![image](https://github.com/fatimaaldrweesh/Wheat-Segmentation/assets/63796712/888a4a7c-827d-48af-b1bb-96310eafdc1c)![image](https://github.com/fatimaaldrweesh/Wheat-Segmentation/assets/63796712/e4706c16-bae1-4b66-b6b3-95fcaf618e44)![image](https://github.com/fatimaaldrweesh/Wheat-Segmentation/assets/63796712/44b97984-b153-4d78-b16d-c14d4ae05256)# Image segmentation for wheats using SOTA Models

## Objectives
   - Develop an image segmentation vision app using SOTA models
   - Evaluate multiple SOTA models: Yolov8-seg, SAM model, U-Net
   - Compare and analyze the performance of each model
   - Use onnxruntime to accelerate inference time

## Pipline
![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/pipline.png)

## Download data from Kaggle
The Global Wheat Head Dataset is led by nine research institutes from seven countries: the University of Tokyo, Institute national de recherche pour agriculture, alimentation et Environment, Arvalis, ETHZ, University of Saskatchewan, University of Queensland, Nanjing Agricultural University, and Roth Amsted Research. These institutions are joined by many in their pursuit of accurate wheat head detection, including the Global Institute for Food Security, Digi tag, Kubota, and Hyphen.
Train: 3422 images 
Test: 10 images 

## Image Segmentation
- We used CVAT to annotate our image. 

![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/cvat.png)

- In CVAT there are three methods to annotate images: polygon, ai tool, and using pre-trained model.

- To achieve one of the purposes of this project which is to learn how to make manual annotation we used polygon annotation for 200 images then we used ai tool to complete our data annotation.

![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/ai%20tool.png)

### Samples from annotation using ai tool. 
<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/s1.png" alt="Image 1" width="200"/>
    <img src="https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/s2.png" alt="Image 2" width="200"/>
    <img src="https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/s3.png" alt="Image 3" width="200"/>
</div>

### The annotation doesn’t fully based on ai tool so we used polygon.
![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/prob.png)

### Number of annotations examples 
| Number og images   | Number of annotations |
| ------------------ | ----------------------|
| 27                 | 875                   |
|49                  | 1766                  |
| 138                | 4893                  |

### Choose the best annotated format from CVAT 
![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/JSON.png)
![2](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/MASK.png)

## Augmentation
- It is a process to increase the number of training data. 
- This process is changes based on the training model we used.
 - We will explained in details in the next section. 

## Models:
![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/models.png)

### YOLOn8-seg:
![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/yolo.png)

### UNET from scratch:
![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/unet%20scratch.png)

### UNET fine tunning:
![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/unet%20finetune.png)

### SAM:
![1](https://github.com/fatimaaldrweesh/Wheat-Segmentation/blob/main/Data/sam.png)














