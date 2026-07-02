# Face Recognition in Python

A simple face recognition application built with Python, dlib, and the `face_recognition` library.

## Features

- Encode known faces from a training dataset
- Recognize faces in unknown images
- Draw bounding boxes and predicted names
- Supports HOG (CPU) face detection

## Technologies

- Python
- dlib
- face_recognition
- Pillow
- NumPy

## Usage

Train:

```bash
python detector.py --train
```

Validate:

```bash
python detector.py --validate
```

Test:

```bash
python detector.py --test -f path/to/image.jpg
```


