# FaceID
project sử dụng framework insightface và tensorflow
# Requiement
- python 3.3+
- tensorflow 2.x
# Setup
`pip install -r setup.txt`
# How to use in your dataset
1. prepare data set
```
/datasets
  /train
    /person1
      + face_01.jpg
      + face_02.jpg
      + ...
    /person2
      + face_01.jpg
      + face_02.jpg
      + ...
    / ...
  /test
```
your dataset is a face image file with size 112x112 or you can use
```
python get_faces_from_video.py
```
to get picture from video, The photo will be saved at unlabeled images
2. Generate face embeddings
```
python faces_embedding.py
```
3. Train
```
python train_softmax.py
```
here is the result

![](/src/outputs/accuracy_loss.png)

4. Run
```
cd src
python recognizer_stream.py
```


