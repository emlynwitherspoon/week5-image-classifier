# Week 5 Project: Smart Image Classifier

**Name: Emlyn Witherspoon**

## Part 1 - Build Your Dataset

### 1.1 Pick a Task

I chose hand gestures using rock, paper, and scissors because they are simple gestures that I can easily capture using my laptop webcam.

### 1.2 Capture Your Images

I used Teachable Machine and my laptop webcam to capture 150 images in total.

- Rock: 50 images
- Paper: 50 images
- Scissors: 50 images

- I captured the images with my hand about 1 to 2 feet away from my laptop webcam.

- ### 1.3 Record Your Conditions
- - Location: I was sitting in my living room chair.
  - - Lighting: My living room ceiling light was on, and I captured the images in the evening.
    - - Background: There was a wall with a painting behind my hand.
      - - Angles: I moved and tilted my hand in different directions while capturing the images.
        - - Distance: My hand was about 1 to 2 feet away from the camera.
- Subject: I used my own hand for all the images.

- ## Part 2 - Train and Measure

### 2.1 Train

I successfully trained my model using 150 images in Teachable Machine.

<img width="960" height="540" alt="Screenshot 2026-11-23 232631 images" src="https://github.com/user-attachments/assets/6dd2a63d-931e-4102-bb6a-c3d1c731459d" />

### 2.2 Test It the Easy Way
| Test | Actual | Prediction | Confidence |
|---|---|---|---|
| 1 | Rock | Rock | 100% |
| 2 | Rock | Rock | 100% |
| 3 | Rock | Rock | 99% |
| 4 | Rock | Rock | 98% |
| 5 | Rock | Rock | 96% |
| 6 | Paper | Paper | 97% |
| 7 | Paper | Paper | 99% |
| 8 | Paper | Paper | 86% |
| 9 | Paper | Paper | 97% |
| 10 | Paper | Paper | 72% |
| 11 | Scissors | Scissors | 52% |
| 12 | Scissors | Scissors | 82% |
| 13 | Scissors | Scissors | 57% |
| 14 | Scissors | Rock | 44% |
| 15 | Scissors | Scissors | 95% |

- Correct predictions: 14 out of 15
- Incorrect predictions: 1
- Overall accuracy: 93.3%



        - 
