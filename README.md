# Monitoring Mask Compliance in Classrooms

## Introduction

In 2020, the Covid-19 pandemic changed the way students attend class in a traditional classroom setting. With schools and universities moving back to in-person instruction, wearing masks in the classroom has become critical to preventing the spread of the virus. However, this only works when everyone is adhering to and following mask wearing guidelines. 

Our team created a computer vision tool to monitor mask compliance by students in the classroom, and detect whether or not a student is wearing a mask. It also allows for certain common actions, such as drinking liquids, to be detected and a valid reason to not wear a mask. To solve this problem, we created both a deep learning and traditional machine learning powered approach.

## Product Overview

The diagram below describes the method we developed to distinguish whether a student was compliant with proper masking guidelines. Using a Yolo v5 model, our tool was retrained to detect people who were masked, unmasked, and drinking.

![CV Module Project_Team6 pptx](https://user-images.githubusercontent.com/31523376/153795005-e6da8b04-6889-44e3-91b7-f217af3dcac7.jpg)

## Data Sources

Both the traditional and deep learning modeling approaches were trained and validated on a corpus of roughly 500 hand-labeled images. Three classes of images (Mask, Unmasked, and Drinking) were acquired from Google and Baidu. The labeled images can be found in our team's Google Drive (https://drive.google.com/drive/u/0/folders/1L99-GBLdlgDMoBE6dzdLzHs0WT9khT5c).

## Demo

The image below displays some of the results from the mask compliance tool. Real examples of both the training data used, and the mode's predictions can be seen below.

![CV Module Project_Team6 pptx (1)](https://user-images.githubusercontent.com/31523376/153797963-a6a0759a-6291-4ad8-b822-0fd866e25df6.jpg)

## Getting Started

First install the requirements necessary to run the python files.

```
pip install requirements.txt
```

### Machine Learning Approach

To solve this problem before using a Deep Learning approach, we were interested in doing some preliminary testing using a classic Machine Learning method. We decided to frame it as a multi-class classification problem so we could try to solve it using a Softmax Regression. The approach was impractical for several reasons, but especially due to the model's inability to learn at the local level and also to handle non-mutually exclusive labels in a single image. Nonetheless, if you'd like to run the code of this approach, you can follow these steps:

After installing all of the requirements, you can execute the file `scripts\train_classic.py`

   * The output will be the accuracy of the classic ML approach on both train and test sets.

Here's an example of how to execute the file using Google [Colab](https://colab.research.google.com/drive/1GvT4BWaAg4-l8CiugQanq653XLqcyCby?usp=sharing).

### Deep Learning Approach

The second approach, as described earlier, and shown in the demo utilizes the Yolo v5 architecture trained on new images of the desired classes. The tool can be called by running the file below:

```
```
