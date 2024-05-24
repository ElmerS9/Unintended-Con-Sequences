# Unintended-Con-Sequences

This is the implementation for my Dartmouth Video Understanding Mini-Conference paper [Unintended Con-Sequences]. Everything added to this repository was used to set the model in a Google Colab Environment, as well as my paper. It includes the code for training and adapting the Oops dataset and pre-trained Kinetics TimeSformer model. This project provides a framework for improving unintentional action prediction for the Oops dataset, which focuses on both human and animal "fails" collected from YouTube videos. 

# Overview 
The main goal of this project, as mentioned above, was to develop a framework for predicting unintentional actions in videos. This involves: 
1. Loading and preprocessing the Oops dataset
2. Adapting the pre-trained TimeSformer to the Oops dataset
3. Fine-tuning the TimeSformer model to the Oops dataset.
4. Analyzing the model's performance on the Oops dataset and improving its accuracy. 

# Preparation and Implementation.
Loading the Oops dataset and TimeSformer model is fairly simple. The authors of both papers have made their data and code readily accessible for download. 
1. Download the Oops dataset [here](https://oops.cs.columbia.edu/data/#download).
2. Download the pre-trained Kinetics-400 Timesformer model [here](https://github.com/facebookresearch/TimeSformer).


It is highly recommended to download the Oops dataset to Google Drive due to its sheer size. The contents of the dataset come in a zipped file called "video_and_anns.tar.gz". Download this folder in your drive and unzip it in the folder. Having it available from the drive helps with loading the videos into the Colab environment by mounting. Once this folder is unzipped, you will have two other files to unzip named 'video.tar.gz' and 'annotations.tar.gz.' Depending on your resources it will take anywhere between 10-20 hours for the data to be unzipped and loaded, or maybe less. 

Once all data is unpacked you will have a folder called 'oops_dataset' this folder will have two subfolders called 'oops_video' and 'annotations'. The video folder will have the val and train video sets, and the annotations folder will have the val.txt and train.txt for training. The annotations folder also contains more annotation data that you can find more about in the datasets README.md. 

In loading the TimeSformer model, the link to its GitHub repository has specific instructions on its installation and all the packages that it requires. You can also reference my Colab for how it is loaded.

In terms of the environment and code, the Google Colab environment in this repo contains all the information of the libraries that are needed along with functions for processing. Keep in mind that the experimental results for this paper were unsuccessful, meaning that not all of the current functions are working.
