# ML Computer Vision Internship Submission

This repository contains multiple computer vision mini-projects delivered as Jupyter notebooks, with a tech report and step-by-step usage notes.

## Repository layout

- `notebooks/`
  - `Animal_Detection/Animal_Detection.ipynb`
  - `Attendance_System/Attendance_System.ipynb` (+ `attendance_records.csv` generated here)
  - `CarColor_Detection/CarColor_Detection.ipynb`
  - `Drowsiness_Detection/Drowsiness_Detection.ipynb`
  - `Nationality_Detection/Nationality_Detection.ipynb`
  - `SignLanguage_Detection/SignLanguage_Detection.ipynb`
- `models/` — place trained model files (e.g., `.h5`, `.pt`, `.pkl`) here
- `assets/` — screenshots, sample media, or any supporting artifacts
- `TechDoc.md.md` — technical documentation and usage steps
- `Data Science Internship Final Report.pdf` — final report
- `requirements.txt` — Python dependencies for running notebooks and GUIs

## Quick start (Windows, Python 3.10–3.11 recommended)

1. Create and activate a virtual environment.
2. Install dependencies:

```powershell
pip install -r requirements.txt
```

Notes:
- Some GUI projects use PyQt (PyQt5 in Animal Detection, PyQt6 in Car Color); both are included here.
- `dlib` can be difficult to build on Windows. If installation fails, consider using a prebuilt wheel, conda, or skip it if you don’t run the drowsiness example that depends on it.

## Running the notebooks

Open the notebooks in VS Code or Jupyter and run cells top-to-bottom. Many notebooks contain pip install cells — you can skip those if you already installed `requirements.txt`.

- Animal Detection: TensorFlow + PyQt5 GUI demo; uses `tensorflow-hub` optionally.
- Attendance System: Face detection (MTCNN), embeddings (FaceNet concept), KNN classifier; writes `attendance_records.csv`.
- Car Color Detection: OpenCV + PyQt6 GUI; YOLO detection is mocked; replace with your model for real inference.
- Drowsiness Detection: Haar cascades + placeholder drowsiness/age; Tkinter GUI demo.
- Nationality Detection: Gradio app with placeholder models; extend with real models.
- Sign Language Detection: TensorFlow CNN/LSTM prototype; Streamlit UI for image upload; optional webcam pipeline.

## Models and data

- Put trained weights and artifacts under `models/`.
- Place reusable inputs (images/videos) under `assets/`.
- Attendance CSV lives at `notebooks/Attendance_System/attendance_records.csv`.

## Tips

- If you run GUI apps (PyQt/Tkinter/Streamlit/Gradio), prefer running locally rather than inside hosted notebook environments.
- For YOLO or other detectors, install the respective libraries and update the code paths as needed.

## Documentation

See `TechDoc.md` for detailed steps, assumptions, and per-project notes.
