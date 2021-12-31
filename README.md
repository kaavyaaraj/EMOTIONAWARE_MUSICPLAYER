# musicplayer
Tensorflow based Emotion detection music player that can recognize up to 7 emotions(Happy, sad, Angry, neutral, Fearful, disgusted, surprised) 

DATASET: https://www.kaggle.com/ananthu017/emotion-detection-fer 


You can either download this dataset or use your own dataset.


*If you are using your own dataset *.


1.once you download the dataset seperate them into 7 folders for each emotion -(Happy, Sad, Neutral, Disgusted, Neutral, Fearful, Surprised).

2.Then save the haarcascade_frontalface_alt.xml and facecrop.py in each of the folder and run facecrop.py file (this is done to convert the image into grayscale images and to resize it to 48*48 ).



We are using Google Colab for training our model for GPU requirements, before you use google colab upload your project folder into your Google drive and mount your drive

COLAB: https://colab.research.google.com/drive/16Ccb0-Mw9ceycYcweNNxdL2K7M2x8tyy?usp=sharing

Colab link and colab is given in the files section above


WORKING:

FOR EASY UNDERSTANDING KEEP THE COLAB FILE *music_player.ipynb* OPEN 


Once you upload files to your google drive and mount the drive in colab,

run this following command:

!python retrain.py --output_graph=retrained_graph.pb --output_labels=retrained_labels.txt --architecture=MobileNet_1.0_224 --image_dir=images

This will train the model and save it in your google drive.


Now run this code which is already available in the colab to start the webcam and take picture 

![image](https://user-images.githubusercontent.com/82087114/147638188-f766428e-9cff-4ed3-a9a4-6d1d2bf8ebb1.png)

The captured image will be saved as photo.jpg


![image](https://user-images.githubusercontent.com/82087114/147638329-6acfaa40-bece-4c7f-aa55-230312134f30.png)
This program recognises faces in a image


Now this code will detect the highest emotion and plays a song from the detected emotion's folder:
![image](https://user-images.githubusercontent.com/82087114/147638377-7d3bff8e-1d8c-4f46-9dc4-d5371e442642.png)

Thank You!




