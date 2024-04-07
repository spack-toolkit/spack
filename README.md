# spack: A Simple Pipeline for Audio Classification using KAPRE

> Term Project, CSC602: Machine Learning, Spring 2024, IIIT Kalyani<br>
**Name**: Nikhil Laxminarayana, Harsh Singh Rawat<br>
**Reg**: ECE/21136/796, ECE/21127/787

We present a pipeline for training classifiers over a diverse dataset to classify instrument samples using frequency domain feature extraction with the help of KAPRE: Keras Audio PREprocessors library. We choose to name this tool **SPACK**. This is also the term project for the course CSC602: Machine Learning, offered in Spring 2024 at IIIT Kalyani.

## Usage and Installation
- Clone this repository, then create a virtual environment using `venv` or `conda` and then to install the dependencies type `pip install -r requirements.txt` in the terminal where the cloned repository resides after activating the virtual environment.
- Then run `clean.py` to generate a `clean` directory. These are the processed wavfiles used for classification. Then run `train.py --model-type conv1d` to train a Conv1D net over the `clean` dataset. 
- Change the value of the model type to `conv2d` and then to `lstm` to store the model parameters into `models` directory.
- The models are now ready to be used to predict values. To predict values over the trainig data, run `predict.py` with the output logs in `y_pred.npy` file.
- Some notebooks in `notebooks/` directory contain code snippets used to generate the confusion matrix and ROC characteristics for the models. 

## References
1. Choi, Keunwoo & Joo, Deokjin & Kim, Juho. (2017). Kapre: On-GPU Audio Preprocessing Layers for a Quick Implementation of Deep Neural Network Models with Keras. [link](https://arxiv.org/abs/1706.05781)