# Monitoring Mask Compliance in Classrooms

## Introduction

In 2020, the Covid-19 pandemic changed the way students attend class in a traditional classroom setting. With schools and universities moving back to in-person instruction, wearing masks in the classroom has become critical to preventing the spread of the virus. However, this only works when everyone is adhering to and following mask wearing guidelines. Our computer vision tool monitors mask compliance by students in the classroom, and detects whether or not a student is wearing a mask. It also allows for certain common actions, such as drinking liquids, to be detected and a valid reason to not wear a mask.

## Getting Started with the Classic ML Approach

To solve this problem before using a Deep Learning approach we were interested in doing some preliminary testing using a classic Machine Learning method and we decided to frame it as a multi-class classification problem so we could try to solve it using a Softmax Regression. The approach was impractical for several reasons, but especially due to the model's inability to learn at the local level and also to handle non-mutually exclusive labels in a single image. Nonetheless, if you'd like to run the code of this approach, you can follow these steps:

After the installation process you can execute the file **`scripts\train_classic.py`**

   * The output will be the accuracy of the classic ML approach on both train and test sets.

Here's an example of how to execute the file using Google [Colab](https://colab.research.google.com/drive/1GvT4BWaAg4-l8CiugQanq653XLqcyCby?usp=sharing).
