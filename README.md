# Sway -AI-Powered Underwater Kick Analysis for Swimmers

Sway is a computer vision system that analyzes underwater kick technique and compares it to an expert swimmer to provide objective, biomechanical feedback.

Using pose estimation, Sway identifies key points of a swimmer's body throughout a kick video, measures three critical joint angles, synchronizes kick cycles between swimmers, and discovers differences in technique.  The result is a set of visualizations, data, and textual feedback meant to help a swimmer improve without paying for expensive private coaching.

This repository contains the complete Sway pipeline, along with sample data to showcase Sway's outputs.

## Features
- Identifies key joints of a swimmer using pose estimation
- Measures joint angles on shoulders, hips, and knees throughout each kick cycle
- Synchronizes kick cycles to enable frame-accurate comparison
- Generates side-by-side comparisons with annotated angles
- Identifies key moments during each kick
- Generates biomechanical feedback for a swimmer at each key moment
- Exports angle comparison data from key moments for further analysis

## Getting Started

### Prerequisites
- Python 3.11 or higher
- pip package manager

### Installation
1. **Clone the repository**
```bash
git clone https://github.com/Rezivann/Sway
cd Sway
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

## Usage

1. **Inserting Videos to compare**

Go into the Data folder and insert the mp4 files of the chosen underwater kick videos.  
Make sure each swimmer has already propelled themself off of the wall at the start of the video.

2. **Selecting Videos within the algorithm**

Within the Scripts folder, open Sway.ipynb.  In the first two lines, there are string variables representing the learner video and the expert video the algorithm will reference.Change the string values of those variables to the file names of the videos you would like to use with the algorithm.

3. **Running the Algorithm**

Run all cells within Sway.ipynb

## Outputs
When you run the algorithm, a folder will be created with in the Outputs folder labled "Output - (number)".  
The highest number represents the most recent trial.  Within each folder is a collection of files representing the various outputs of the algorithm.

### Example Inputs

Learner Video:

https://github.com/user-attachments/assets/654ca411-711b-42bf-8cc9-00b4f5167ad5

Expert Video:

https://github.com/user-attachments/assets/11afdf44-2e0f-4cc9-9506-7b82bd2c5ac9

### Videos
1. Annotated Learner's Video - the learner's video but with their joint angles and angle differences annotated.

https://github.com/user-attachments/assets/2536bf72-c39f-401f-817a-fd4dfbbbb8d2

2. Annotated Learner's Video (Slowed) - Same as Annotated Learner's Video but when angle comparisons are being made, the video plays at 25% speed.

https://github.com/user-attachments/assets/ddda712c-d07c-4844-9c61-2e3844a80fb4
   
3. Key Moments Video - video that cycles through frames of the original annotated video where the thigh-calf angle is at its minimum and maximum values for each kick.

https://github.com/user-attachments/assets/b3c34143-32ca-42c4-9552-9eaef8388854

4. Side-by-Side Comparison - video that shows learner's video on top with angles and angle differences annotated as well as the expert's video with their angles on the bottom.  The kick cycles are synced up visually to show exact differences in technique for each frame.


https://github.com/user-attachments/assets/d2124623-a33a-4309-aba8-44f6e7379c07

5. Side-by-Side Comparison (Slowed) - Same as the Side-by-Side Comparison but played at 25% speed.

https://github.com/user-attachments/assets/7e86d040-a8b0-495b-a60b-d2e861d8c6fa



### Data and Feedback
1. DifferenceData.csv - Tabular data of the body angles of the learner and expert at each key moment.  The differences between these angles is included as well.
2. Feedback.txt - Gives biomechanical advice for the learner at each of the moments observed in the Key Moments Video

