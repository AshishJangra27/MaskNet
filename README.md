# MaskNet
This project is about building a system which can detect whether a person is wearing mask or not on an image or live webcam video using Deep Learning and Computer Vision.

I've used MobileNet for this purpose and then use transfer learning on it. The dataset used in this project is available on https://github.com/prajnasb/observations repository. Lets discuss about each code fire one by one.

# FaceMask_Train.ipynb 
This code file downloads the dataset. Preprocess it and then Train our neural network. This network has been trained using transfer learning of MobileNet. We've achieved a testing accuracy or 99.2% which is really good. We are saving the model with name 'MaskNet.hdf5' after training.

# Single_Image _Detection.ipynb
This code file first loads the pretrained model. We need to add the path of the image which we want to process. Then the model predict wherther mask is detected or not. (0 = 'Not Masked', 1 = 'Masked). For testing you can use images which is present in the repository named as masked and unmasked.

# live_without_face_detection.ipynb
This code file take the live video feed from the webcam and directly pass each frame into the trained model. Then it writes on the video window that you've wearing a mask('Masked') or not('UnMasked').

# live_with_face_detection.ipynb
This code file take the live video feed from the webcam and then find the faces from the given frames. Then we pass only those framed to the trained model. Then it draw the rectangle on the detected face of video window. If you wear the mask then the drawn rectangle colour is Green and if you don't wear the mask then rectangle colour is Red. 

# live_with_face_detection.ipynb might not work well because when we wear mask then haarcascade file can't detect your face much efficiently. You can use YOLO for detecting faces.

If you like this project then make sure to give this repository a Star. If you have any doubt then make sure to ask me on https://www.linkedin.com/in/ashish-jangra.

Happy Learning!
