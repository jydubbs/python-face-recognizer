# Face Recognition Tool in Python

This project implements a command-line face recognition pipeline that encodes known faces, recognises unknown faces, and visualises predictions using Python and dlib.

**Note**

This project was developed and tested on an Apple Silicon (M-series) Mac using Conda. Installation instructions have been adapted accordingly.

## Features

- Encode known faces from a labelled training dataset
- Match unknown faces against previously encoded identities
- Draw bounding boxes and predicted names
- Supports HOG (CPU) face detection

## Technologies

- Python 3.10
- dlib
- face_recognition
- NumPy
- Pillow
- argparse
- pickle

## Installation

Clone the repository:

```bash
git clone https://github.com/jydubbs/python-face-recognizer.git
cd face-recognizer
```

Create a Conda environment:

```bash
conda create -n face_recognizer python=3.10
conda activate face_recognizer
```

Install dependencies:

```bash
conda install -c conda-forge dlib numpy pillow
pip install -r requirements.txt
```

## Usage

Train the face encoder using known faces:

```bash
python detector.py --train
```

Validate images:

```bash
python detector.py --validate
```

Test an image:

```bash
python detector.py --test -f validation/example.jpg
```

## Example output

Input image: 

<img width="212" height="215" alt="Screenshot 2026-07-02 at 16 29 43" src="https://github.com/user-attachments/assets/4177e4a7-6b77-4f26-9a13-233d8a332f08" />

Output: 

<img width="216" height="216" alt="Screenshot 2026-07-02 at 16 20 54" src="https://github.com/user-attachments/assets/92b23f8f-5a88-40e1-a2e4-d1e32e893749" />

## Technical Concepts Demonstrated

- Building command-line Python applications with argparse
- Face detection using HOG-based models
- Generating and comparing face embeddings using dlib
- Image manipulation with Pillow
- Serializing trained encodings with pickle
- Working with Python virtual environments and Conda
- Debugging package compatibility issues on Apple Silicon

## Future Improvements

- Add webcam support for real-time recognition
- Replace HOG with CNN-based detection
- Store encodings in a database instead of pickle
- Build a Streamlit web interface
- Support multiple face recognition thresholds
- Add unit tests

## Project Structure

```text

face-recognizer/
│
├── detector.py
├── requirements.txt
├── README.md
├── .gitignore
├── training/
├── validation/
└── output/

```

## Motivation

This project was completed to gain an understanding of modern face recognition pipelines, including facial embedding generation, similarity matching, image processing, and command-line application development in Python.


## Acknowledgements

This project was built while following and extending the tutorial **"Build Your Own Face Recognition Tool With Python"** by Kyle Stratis (Real Python, updated April 24, 2023).

While implementing the project, I adapted the code to run on Apple Silicon (M-series) Macs, resolved dependency and compatibility issues with modern Python tooling, and used it as a learning exercise to understand face recognition pipelines, command-line applications, and Python package management.

