# Celebrity Face Recognition Project

A comprehensive face recognition system using Python and the face_recognition library to identify celebrity faces with high accuracy.

## Features

- **Deep Learning Face Recognition**: Uses state-of-the-art face encodings with 99.38% accuracy
- **Group Photo Recognition**: Detect and identify multiple faces in a single image
- **Expandable Celebrity Database**: Easily add new celebrities by downloading their photos
- **Facial Landmark Detection**: Visualizes 68 facial landmark points
- **Multiple Recognition Methods**: Compares deep learning vs landmark-based approaches
- **Batch Processing**: Process multiple images at once
- **Visual Analysis**: Side-by-side comparisons with similarity scores
- **Real-world Testing**: Process actual group photos and magazine images

## Requirements

- Python 3.7+
- Jupyter Notebook

## Installation

1. Clone this repository:
```bash
git clone https://github.com/mingqxu7/faceRecognition.git
cd faceRecognition
```

2. Install required packages:
```bash
pip install face-recognition opencv-python matplotlib numpy pandas
```

Note: Installing `face-recognition` will also install `dlib` which may take some time to compile.

## Project Structure

```
faceRecognition/
├── celebrity_face_recognition.ipynb  # Main notebook with all code
├── README.md                        # This file
└── .gitignore                       # Git ignore file
```

**Note**: The `images/` folder will be created automatically when you run the notebook. Images are downloaded from Wikipedia Commons and are not included in the repository.

## Usage

1. Open Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `celebrity_face_recognition.ipynb`

3. Run all cells in order. The notebook will:
   - Create an `images/` directory
   - Download celebrity images automatically from Wikipedia Commons
   - Load and encode known faces
   - Demonstrate single and group face recognition
   - Add new celebrities to the database (Shameless cast members)
   - Process real-world group photos
   - Compare different recognition methods
   - Analyze accuracy and performance

## Key Components

### 1. Face Recognition with Deep Learning
- Uses 128-dimensional face encodings
- Compares unknown faces against known celebrity database
- Achieves high accuracy with proper threshold tuning

### 2. Group Photo Recognition
- Detects multiple faces in a single image
- Identifies each person with confidence scores
- Draws bounding boxes with color-coded results (green=recognized, red=unknown)

### 3. Expandable Celebrity Database
- Download celebrity photos from verified URLs
- Automatically encode faces and add to database
- Currently includes 6 celebrities: Obama, Musk, Tiger Woods, and 3 Shameless actors
- Easy to extend with new celebrities

### 4. Facial Landmark Detection
- Detects 68 facial landmark points
- Visualizes features like eyes, nose, mouth, chin
- Color-coded visualization for different facial features

### 5. Comparison Analysis
- Landmark-based vs Deep Learning methods
- Shows why geometric features alone aren't sufficient
- Demonstrates superiority of deep learning approach

### 6. Real-world Testing
- Process magazine photos and group images
- Handle various lighting conditions and poses
- Test with actual celebrity group photos

### 7. Accuracy Analysis
- Tests different tolerance thresholds
- Calculates false positives and false negatives
- Helps optimize threshold selection

## Recognition Accuracy

The face_recognition library achieves:
- **99.38% accuracy** on Labeled Faces in the Wild benchmark
- Based on dlib's ResNet model
- Trained on 3+ million faces
- Robust to variations in lighting, pose, and expression

## Best Practices

1. **Image Quality**: Use high-resolution, well-lit images
2. **Threshold Selection**: Default 0.6 works well; adjust based on your needs
3. **Face Alignment**: Library handles this automatically
4. **Multiple Faces**: Can detect and recognize multiple faces in one image

## Common Issues

1. **No face detected**: Ensure image has clear, front-facing face
2. **Wrong matches**: Lower the tolerance threshold for stricter matching
3. **Installation issues**: dlib compilation requires cmake and build tools

## Technologies Used

- **face_recognition**: High-level face recognition library
- **dlib**: Underlying C++ library for face detection and recognition
- **OpenCV**: Image processing and visualization
- **NumPy**: Numerical computations
- **Matplotlib**: Plotting and visualization
- **Pandas**: Data analysis and visualization

## Adding New Celebrities

The notebook makes it easy to expand the celebrity database:

1. **Find working image URLs** for the celebrities you want to add
2. **Run the download cells** to fetch their photos
3. **Encode their faces** automatically into the database
4. **Test recognition** on new group photos

Example celebrities already included:
- **Political Leaders**: Barack Obama
- **Tech Entrepreneurs**: Elon Musk
- **Athletes**: Tiger Woods
- **TV Stars**: Shameless cast (William H. Macy, Emmy Rossum, Jeremy Allen White)

## Future Enhancements

- Add more celebrities and TV show casts to the database
- Implement real-time video recognition
- Create a web interface for easy photo uploads
- Add age and emotion detection
- Implement face verification (1:1) vs identification (1:N)
- Support for custom training on personal photo collections

## License

This project is for educational purposes. The face_recognition library is licensed under the MIT license.

## Acknowledgments

- Built using Adam Geitgey's [face_recognition](https://github.com/ageitgey/face_recognition) library
- Uses dlib's state-of-the-art face recognition model
- Celebrity images sourced from Wikipedia Commons