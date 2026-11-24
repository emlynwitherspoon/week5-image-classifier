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

### 2.3 Predict

No, I don't think the accuracy will stay at 93.3% because I trained the model using my own hand in the same room and lighting.

## Part 3 - Break It

### 3.1 Run Four Hostile Tests

I tested my model under four different conditions to see how well it would perform outside of its original training environment.

| Test Condition | Rock (%) | Paper (%) | Scissors (%) |
|---|---|---|---|
| Different place | 100, 99, 98, 99, 99 | 99, 97, 100, 95, 99 | 99, 95, 80, 75, 99 |
| Different light | 99, 100, 100, 98, 99 | 97, 94, 99, 100, 100 | 72, 67, 81, 90, 96 |
| Different distance or angle | 90, 81, 60, 72, 75 | 21, 50, 18, 19, 98 | 94, 72, 66, 82, 35 |
| Someone else's hand | 99, 86, 82, 98, 15 | 59, 39, 90, 87, 70 | 16, 30, 33, 15, 17 |

### 3.2 Report the Damage

| Test | Accuracy | Worst failure |
|---|---|---|
| Part 2 baseline | 14/15 (93.3%) | — |
| Different place | Not fully recorded | Paper predicted as Rock at 99% |
| Different light | Not fully recorded | Scissors confidence dropped to 67% |
| Different distance | Not fully recorded | Paper confidence dropped to 18% |
| Someone else's hand | Not fully recorded | Scissors confidence dropped to 15% |

The test using someone else's hand showed the biggest drop in confidence, especially for scissors. This suggests that the model was paying attention to the appearance of my hand instead of just the hand gestures.

## Part 4 - Diagnose and Fix One Thing

### 4.1 Form a Hypothesis

I think my model learned the appearance of my own hand instead of focusing only on the shape of each gesture.         

### 4.2 Change One Thing and Retrain

I added images of my daughter's hand to the existing dataset for rock, paper, and scissors. I then retrained the model and tested it again using her hand.

### 4.3 Did It Work?

Before retraining, the model struggled to recognize my daughter's hand, especially scissors. After retraining, the model performed better at recognizing her gestures. My recorded results suggest an improvement, but I did not fully record the accuracy before retraining, so I cannot calculate the exact improvement.
