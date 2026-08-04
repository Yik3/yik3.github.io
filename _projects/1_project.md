---
layout: page
title: Gaze-Guided Active Perception for Long Horizon Imitation Learning
description: Human operator's gaze gives us crucial learning information to long-horizon task segmentation
img: assets/img/gaze.png
importance: 1
category: Robotics
related_publications: true
---
<!-- 下面是文字叙述部分 -->

### Step 1
Data Collection(ALOHA Setup + Meta Aria Glasses)：
* Collect Paired Human Data with leader arms and Aria Glasses. The Robot Data is exactly the same as humans since we are using teleoperation. 
* Post Process the data with a 1D Convolution kernel as a weighted average to denoise. 
* Synchronize the data to form datapairs for dataloaders. 

### Step 2
Find the Goal Gaze and Dissected the task
* Using drift, velocity, acceleration, set a tuned threshold and dissect the task into several subtasks. 
* Since exact gaze position is very noisy from human operator, we focused on goal gaze. 

### Step 3
Gaze Prediction and Task Prediction
* With the gaze signal, add a gaze-foveation: gaussain-based masks that blurs the observation thats too far from the gaze point. A task selector is then trained to select specific subtask. 

### Step 4
Goal-conditioned Policy Training
* Uses an ACT backbone with subtask and goal gaze as extra channels to the model, train the policy

View our poster here:
<br>

<!-- 下面是嵌入 PDF Poster 的代码 -->
<!-- 请将 data 和 href 里的路径替换为你实际 PDF 文件存放的路径，例如 /assets/pdf/poster.pdf -->

<div class="pdf-container" style="margin-top: 30px; text-align: center;">
    <object data="/assets/pdf/gaze_poster.pdf" type="application/pdf" width="100%" height="800px" style="border: 1px solid #ccc; border-radius: 4px;">
        <p>Cannot view in your browser.<a href="/assets/pdf/gaze_poster.pdf">Click here to download the poster.</a></p>
    </object>
</div>