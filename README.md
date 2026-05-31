# Sway - A Human Pose Estimation Algorithm Improving Underwater Kick Technique

This repository contains the code that comprises this algorithm, as well as sample videos to compare using the algorithm.

## Instillation

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


### Videos
1. Annotated Learner's Video - the learner's video but with their joint angles and angle differences annotated.
2. Annotated Learner's Video (Slowed) - Same as the annotated video but when angle comparisons are being made, the video plays at 25% speed.
3. Key Moments Video - video that cycles through frames of the original annotated video where the thigh-calf angle is at its minimum and maximum values for each kick
4. Side-by-Side Comparison - video that shows learner's video on top with angles and angle differences annotated as well as the expert's video with their angles on the bottom.  The kick cycles are synced up visually to show exact differences in technique for each frame.

### Data and Feedback
1. DifferenceData.csv - Tabular data of the body angles of the learner and expert at each key moment.  The differences between these angles is included as well.
2. Feedback.txt - Gives biomechanical advice for the learner at each of the moments observed in the Key Moments Video

