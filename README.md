# License Plate Recognition

A Python-based license plate recognition system.
The goal of the project is to detect and recognize license plates from video sequences under varying conditions, producing accurate and real-time results in a specified output format.

## Project Objective

Given an input video, detect the license plate regions and extract alphanumeric text with high accuracy. The system must support evaluation through a standardized testing pipeline and output results in a CSV format.

## Input
- Example input video: `dataset/dummytestvideo.avi`
## Output
- Example output: `dataset/sampleOutput.csv`
## Project Structure
- `main.py` – Entry point of the pipeline.
- `CaptureFrame_Process.py` – Handles frame extraction from video.
- `Localization.py` – Detects license plate regions.
- `Recognize.py` – Performs character recognition on localized plates.
- `helpers/` – Optional utility scripts and references.
- `evaluation.py` – Score calculation.
- `evaluator.sh` – Script for running the full evaluation.
- `requirements.txt` – Python dependencies.

## Pipeline Overview

1. `main.py` orchestrates frame extraction, localization, and recognition.
2. `evaluator.sh` runs `main.py` and evaluates the output using `evaluation.py`.
3. Outputs are scored based on accuracy, position, and character correctness.

## Setup Instructions

1. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

2. (Recommended) Use a virtual environment:
    ```bash
    python -m venv env
    source env/bin/activate  # Linux/Mac
    env\Scripts\activate     # Windows
    ```

3. Common troubleshooting:
    - Missing `cv2`? Run: `pip install opencv-python`
    - FFmpeg errors? Install it:
        - Windows: [Download here](https://ffmpeg.org/download.html)
        - Linux: `sudo apt install ffmpeg`
        - Mac: `brew install ffmpeg`

## Evaluation

The evaluation script computes detection and recognition scores.
