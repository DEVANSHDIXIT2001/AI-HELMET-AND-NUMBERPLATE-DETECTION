# AI-HELMET-AND-NUMBERPLATE-DETECTION

Our main motive behind Helmet and Number Plate Detection and Recognition was to first detect if someone is wearing a helmet or not, if he is wearing it, no problem, but if not, detect his number plate and send an e-challan to him.




Line 1–8 — Importing required libraries.
Line 10 — Allow TensorFlow to use GPU.
Line 12 — Read the network weights from yolo files. These ‘yolo.weights’ is the file which we trained just to detect bikes and number plates.
Line 13–14 — If you want to use GPU, set the backend and target to CUDA.
Line 17–18 — Load the CNN model we trained to detect helmets.


Line 20 — VideoCapture object to read frames from the video feed.
Line 21 — A color array which we will use later.
Line 23–27 — This writer will help write our output frames to a video file using cv2.VideoWriter().
Line 29–37 — This function will be provided with an image and the model will predict whether there is a helmet or not in the image.
Line 39–40 — Get the output layers to take the output from them in further steps.
Line 46–49 — Read the frames from the video file, resize them and get their height and width.
Line 51 — Use cv2.dnn.blobFromImage() to create a blob from the image and to use this blob as input to our network.
Line 53 — Set this blob as input to our network.
Line 54 — Flow this blob through the network and get the outputs.
Line 60–76 — Get the outputs from the network.
Line 78 — Get the indexes of the boxes which we will not consider due to Non-Maximum Suppression.
Line 80–99 — Draw a green box around bikes and a red box around number plates. Detect if there is a helmet or not and print that.
Line 102–103 — Write the output images as a video.
Line 105–106 — Break the code if someone hits the ESC key.
