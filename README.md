# ISIC 2018: Lesion Attribute Detection
Melanoma is the most deadly form of skin cancer worldwide. Many efforts have been made for early detection of melanoma. The International Skin Imaging Collaboration (ISIC) hosted the 2018 Challenges to help the diagnosis of melanoma based on dermoscopic images. We describe our solutions for the task 2 of ISIC 2018 Challenges. We present two deep learning approaches to automatically detect lesion attributes of melanoma, one is a multi-task U-Net model and the other is a Mask R-CNN based model. Our multi-task U-Net model achieved a Jaccard index of 0.433 on official test data, which ranks the 5th place on the final leaderboard.

## How to run the pre-trained model on the ISIC2018 test data

#### 1. Create a Python environment
```
conda create -n isic2018 python=3
source activate isic2018
```

#### 2. Install necessary packages
```
pip install -r requirements.txt
```
Those are the packages installed in my environment and many packages are not necessarily needed to run the pretrained model. But for ease of use, I just dumped all the installed packages into one file.

#### 3. Clone this repo
```
git clone https://github.com/chvlyl/ISIC2018.git
cd ISIC2018
```

#### 4. Download the ISIC2018 test images
All the ISIC2018 test images are in jpg format. Save those images into a folder.

#### 5. Donwload the pretrained model weights
The trained model weights can be downloaded [here](https://drive.google.com/drive/folders/1oxA7AXwnIug2H91r_49qthekz6UP47rc?usp=sharing)

#### 6. Run the pretrained model on test data
```
python submission.py --image-path test_image_path --model-weight model.pt
```
By default, the predicted masks will be saved in the prediction folder

## Further improvement

## Reference	
1. For more details, please check our paper: Eric Z. Chen, Xu Dong, Junyan Wu, Hongda Jiang, Xiaoxiao Li, Ruichen Rong. Lesion Attributes Segmentation for Melanoma Detection with Deep Learning. bioRxiv 2018 [https://doi.org/10.1101/381855]
2. Some of the code was adapted from this [repo](https://github.com/ternaus/robot-surgery-segmentation)
