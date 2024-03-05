# Introduction 
ECM is an Endoscopic Classification Model that, using the deep learning model CNN, predicts the presence of an abnormality within an endoscopic image. 
For this purpose, we have implemented the classes:

1.	Polyp: This class is assigned when the model detects the presence of a polyp.
2.	Hemorrhoid: This class is assigned when the model detects the presence of a hemorrhoid.
3.	Ulcerative Colitis Grade 0:This class is assigned when the model detects the presence of an Ulcerative Colitis Grade 0.
4.	Ulcerative Colitis Grade 1: This class is assigned when the model detects the presence of Ulcerative Colitis Grade 1.
5.	Ulcerative Colitis Grade 2: This class is assigned when the model detects the presence of Ulcerative Colitis Grade 2.
6.	Ulcerative Colitis Grade 3: This class is assigned when the model detects the presence of Ulcerative Colitis Grade 3.
These classes have been defined based on the dataset used. Due to time and space constrictions, we have limited them to 8 classes.
The goal of ECM is to identify potential risks and enhance patient care.

The dataset used for training and testing is The HyperKvasir Dataset.
 

## Methodology 
Making use of Plotly and Matplotlib, we have visualized our training data as images.

Each set of images, based on previous labels, is represented with their pixel values in the form of a histogram.

Furthermore, data is explored by checking for null values in the training dataset and preprocessed by resizing each image to decrease time and space complexity. Since the dataset used has no existing outliers along with the absence of null values, affirming its suitability for the model to be built on.

By using VGG-16 (CNN), we are building a deep learning model on the image dataset as well as generating the classes. 

The input consists of a set of or a singular Lower GI endoscopic image tested against the learned classes.

Furthermore, we are using metrics including  f1-score, precision, recall, and accuracy to evaluate our model. 



## Findings:

| Metric | Value (%) |
|--------|-----------|
| Recall | 92.14     |
| F1 Score | 91.41    |
| Precision | 92.51    |
| Accuracy | 92.14     |


Since the cost of false negatives is high, recall is designated as the most important evaluation measure. The current model provides an adequate value of 92.14% which ensures its reliability. 
However, it still suggests that the model can be further improved by fine-tuning the training dataset to achieve even higher reliability in its predictions.

## Future Implications:
The future implications of PCM lie in continuous fine-tuning of the model, and alignment with emerging technologies. These efforts have the potential to significantly enhance diagnostic tools in gastroenterology, particularly in image classification, ultimately resulting in improved patient outcomes and more efficient healthcare interventions.

## Resources:
The entirety of the training and testing data has been provided by  https://osf.io/mh9sj/ which is an exploratory model on GI endoscopic images. This source was chosen due to the clinical credibility as mentioned.

Other sources: https://springernature.figshare.com/articles/dataset/Metadata_record_for_HyperKvasir_A_comprehensive_multi-class_image_and_video_dataset_for_gastrointestinal_endoscopy/12759833?file=24463475

https://www.mathworks.com/help/deeplearning/ref/vgg16.html
