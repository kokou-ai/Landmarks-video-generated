# Sign Language Landmarks Video Generator

This project converts original sign language videos into videos with annotated landmarks using MediaPipe and OpenCV. The generated videos highlight key landmarks on the face, body, and hands, making it easier to analyze and interpret sign language data for machine learning applications.

## Installation

To get started, you'll need to install the required packages. You can install them using pip:

```bash```
pip install mediapipe tensorflow transformers

## Project Overview

    Input: Original sign language videos.
    Output: Videos with annotated landmarks, along with a dataset containing the landmark coordinates in .npy format.

## Key Features

    Face Landmarks: Annotates facial features.
    Body Landmarks: Highlights body pose connections.
    Hand Landmarks: Differentiates between left and right hands with custom colors.

## How to Use

    Process Video: The script processes each video to extract and annotate landmarks.
    Generate Video: After processing, you can generate a new video file with the annotated landmarks.

## Example Usage

python

### Define the path to the video
video_path = "video_data/val/computer/12335.mp4"

#### Process the video to extract landmarks
video_landmarks = process_video(video_path)

#### Generate the landmarks video
generate_video(video_landmarks, "computer_landmarks.mp4", 480, 640)

Create Dataset

For each video, a matrix of shape (60, 543, 3) is created, where:

    ```
    60 is the number of frames.
    543 is the number of landmarks (468 for face, 33 for pose, 21 for each hand).
    3 represents the (x, y, z) coordinates of each landmark.```

The dataset is divided into training, validation, and test sets, with data saved in .npy format for use in machine learning models.
Dataset Structure

The dataset is organized into the following directories:

    train/
    val/
    test/

Each directory contains subfolders named after the corresponding labels.
Contributing

Contributions are welcome! If you find a bug or want to add new features, feel free to submit a pull request.
License

This project is licensed under the MIT License - see the LICENSE file for details.


This README provides an overview of the project, installation instructions, and usage examples. Feel free to adjust any section as needed!
