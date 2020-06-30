# Classification and Segmentation of Covid-19 CT Scans**
This study was concerned with the challenge of coronavirus disease (COVID-19) detection in chest X-ray and Computed Tomography (CT) scans, and the classification and segmentation of related infection manifestations. In the first stage, Inception-v3 deep model was fine-tuned for COVID-19 recognition using multi-modal learning, i.e., using X-ray and CT scans attained accuracy of 99.4%. The second stage of the proposed pipeline dealing with different types of infection manifestations.
The former features a convolutional neural network architecture for recognizing three types of manifestations,(i.e., ground glass opacity, Consolidation and Pleural effusion) while the latter transfers learning from another knowledge domain, namely, pulmonary nodule segmentation in CT scans, to produce binary masks for segmenting the regions corresponding to these manifestations. The proposed pipeline also features specialized streams in which multiple deep models are trained separately to segment specific types of infection manifestations. It achieved an increase of approximately 4% and 7% for dice coefficient and mean intersection-over-union (mIoU), respectively, while achieving 60% reduction in computational time, compared to the recent literature.


***COVID-19 Classification using Inception-V3:***
Our classification code is based on https://github.com/googlecodelabs/tensorflow-for-poets-2

COVID-19 X-ray image data collection from:
https://github.com/ieee8023/COVID-chestxray-dataset

***COVID-19 Segmentation using Deeplab-V3+:***
This repo attempts to reproduce Encoder-Decoder with Atrous Separable Convolution for Semantic Image Segmentation (DeepLabv3+) in TensorFlow for semantic image segmentation on the COVID-19 dataset. The implementation is largely based on transfer learning from another knowledge domain, namely, pulmonary nodule segmentation in CT scans, to produce binary masks for segmenting the regions corresponding to these manifestations using modified aligned exception as a feature extractor.

https://www.mdpi.com/2075-4418/10/3/131
https://github.com/rishizek/tensorflow-deeplab-v3


Setup Requirements:

    tensorflow >=1.6
    numpy
    matplotlib
    pillow
    opencv-python

You can install the requirements by running pip install -r requirements.txt.

Dataset Preparation
This project uses the TFRecord format to consume data in the training and evaluation process

In order to generate training labels for the dataset, we used COVID-19 CT segmentation dataset
[http://medicalsegmentation.com/covid19/](http://medicalsegmentation.com/covid19/)

![Deeplab Architecture](Architecture.png)
![Deeplab Visualization](visualization.png)
![inception-v3 result](result.png)
## References
1. EL-Bana, S.; Al-Kabbany, A.; Sharkas, M. [A Two-Stage Framework for utomated Malignant Pulmonary Nodule Detection in CT Scans.](https://www.mdpi.com/2075-4418/10/3/131) _Diagnostics_  **2020**, _10_, 131.
2. El-bana, Shimaa, Ahmad Al-Kabbany, and Maha Sharkas. ["A Multi-Task Pipeline with Specialized Streams for Classification and Segmentation of Infection Manifestations in COVID-19 Scans."](https://www.medrxiv.org/content/10.1101/2020.06.24.20139238v1) _medRxiv_ (2020).


