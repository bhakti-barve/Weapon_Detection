# yolov3 and yolov4-custom-functions
## For YOLOs Using Tensorflow (tf, .pb model)
To implement YOLOv4 using TensorFlow, first we convert the .weights into the corresponding TensorFlow model files and then run the model.

##YOLOv3
# Convert v3 darknet weights to tensorflow
## yolov3
python save_model.py --weights ./data/yolov3.weights --output ./checkpoints/yolov3-416 --input_size 416 --model yolov3 

# Run yolov3 tensorflow model
python detect.py --weights ./checkpoints/yolov3-416 --size 416 --model yolov3 --images ./data/images/g2.jpg

# Run yolov3 on video
python detect_video.py --weights ./checkpoints/yolov3-416 --size 416 --model yolov3 --video ./data/video/gun.mp4 --output ./detections/results.avi

# Run yolov3 on webcam
python detect_video.py --weights ./checkpoints/yolov3-416 --size 416 --model yolov3 --video 0 --output ./detections/results.avi

###---------------------------------------------------------------------------------------###

##YOLOv4
# Convert v4 darknet weights to tensorflow
## yolov4
python save_model.py --weights ./data/yolov4.weights --output ./checkpoints/yolov4-416 --input_size 416 --model yolov4 

# Run yolov4 tensorflow model
python detect.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --images ./data/images/g2.jpg

# Run yolov4 on video
python detect_video.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --video ./data/video/gun.mp4 --output ./detections/results.avi

# Run yolov4 on webcam
python detect_video.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --video 0 --output ./detections/results.avi

###---------------------------------------------------------------------------------------###

### Result Image(s) (Regular TensorFlow)
You can find the outputted image(s) showing the detections saved within the 'detections' folder.
### Result Video
Video saves wherever you point --output flag to. If you don't set the flag then your video will not be saved with detections on it.

