# Sway: AI-Powered Underwater Kick Analysis for Swimmers

Sway is a computer vision system that analyzes underwater kick technique and compares it to an expert swimmer to provide objective, biomechanical feedback.

Using pose estimation, Sway identifies key points of a swimmer's body throughout a kick video, measures three critical joint angles, synchronizes kick cycles between swimmers, and discovers differences in technique.  The output is a set of visualizations, data, and textual feedback meant to help a swimmer improve without having to pay for expensive private coaching.

This repository contains the Sway pipeline, along with sample data to showcase Sway's outputs.

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

1. **Add Videos**

Place two underwater kick videos that you want to compare in the Data folder. 

For the best results:
- Videos should be recorded underwater
- Videos should be recorded strictly from the side of the swimmer
- The swimmer should have already pushed off of the wall by the start of the video
- One video should represent the learner
- One video should represent the expert swimmer

2. **Selecting Videos**

Open Scripts/Sway.ipynb.  At the top of the notebook, there are two variables storing the file names of the learner and expert videos.  Replace them with your desired file names.

3. **Run the Pipeline**

Run all cells in Sway.ipynb

## Outputs
After execution, a new folder will be created in the Outputs folder:

Output - 1
Output - 2
Output - 3
...

The folder with the highest number contains the most recent analysis.

Each output folder contains visualizations, comparison videos, biomechanical data, and textual feedback for the learner to improve from.

### Example Inputs

Learner Video:

https://github.com/user-attachments/assets/654ca411-711b-42bf-8cc9-00b4f5167ad5

Expert Video:

https://github.com/user-attachments/assets/11afdf44-2e0f-4cc9-9506-7b82bd2c5ac9

### Videos
1. Annotated Learner's Video - Displays the learner's kick cycles with body angles (pink) and angle differences (red/green) annotated.  Red indicates that the learner's angle is too high while green indicates that their angle is too low.

https://github.com/user-attachments/assets/2536bf72-c39f-401f-817a-fd4dfbbbb8d2

2. Annotated Learner's Video (Slowed) - Same as the video above, but comparison moments are played at 25% speed.

https://github.com/user-attachments/assets/ddda712c-d07c-4844-9c61-2e3844a80fb4
   
3. Key Moments Video - Shows annotated frames where the knee angle is at its maximum and minimum values during each kick.

https://github.com/user-attachments/assets/b3c34143-32ca-42c4-9552-9eaef8388854

4. Side-by-Side Comparison - Shows learner and expert swimmers' synchronized kick cycles with annotated angles, enabling direct side-by-side comparison.


https://github.com/user-attachments/assets/d2124623-a33a-4309-aba8-44f6e7379c07

5. Side-by-Side Comparison (Slowed) - The comparison video played at 25% speed

https://github.com/user-attachments/assets/7e86d040-a8b0-495b-a60b-d2e861d8c6fa



### Data and Feedback

1. DifferenceData.csv - Contains body angle measurements at each key moment for both swimmers and the calculated differences between them.
2. Feedback.txt - Provides technique recommendations based on the observed differences between the learner and expert.

