🎯 Real-Time Face Detection Using OpenCV (Beginner Project)

This beginner-friendly project demonstrates real-time face detection using Python and OpenCV. The system captures your webcam feed and identifies human faces using the Haar Cascade Classifier.


🚀 Features

Real-time face detection through webcam

Uses Haar Cascade face model

Lightweight and fast

Clean and understandable code

Perfect for beginners in Computer Vision


🧠 What I Learned

Basics of Computer Vision

How Haar Cascade models work

Using OpenCV for image processing

Capturing live video feed

Frame-by-frame detection

Drawing bounding boxes on faces


🛠️ Tech Stack

Python 3.x

OpenCV (cv2)


📌 Code Snippet

import cv2

face_cap = cv2.CascadeClassifier("haarcascade_frontalface_default.xml")
video_cap = cv2.VideoCapture(0)

while True:
    ret, frame = video_cap.read()
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

    faces = face_cap.detectMultiScale(gray, 1.1, 6)

    for (x, y, w, h) in faces:
        cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)

    cv2.imshow("Video Live", frame)

    if cv2.waitKey(10) == ord("a"):
        break

video_cap.release()
cv2.destroyAllWindows()




🔮 Future Improvements

Eye detection

DNN-based (Deep Learning) face detection

Emotion detection

Multiple people tracking

Face recognition (Name + ID)


⭐ If you like this project, consider giving it a star on GitHub!

