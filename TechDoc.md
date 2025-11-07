\# 🧠 Technical Documentation: Machine Learning Computer Vision Internship Projects



> \*\*Internship Period\*\*: 24 September – 24 November 2025  

> \*\*Author\*\*: \Mandar Kajbaje 

> \*\*Contact\*\*: \mandarkajbaje@gmail.com 

---



\## 🗂️ Folder Structure



The submission archive is organized for clarity and easy execution:

📁 ML\_ComputerVision\_Internship\_Submission\_Mandar\_Kajbaje/

│

├── 📄 Internship\_Report.pdf ← Complete report in PDF format

├── 📄 TechDoc.md ← You are here!

├── 📄 requirements.txt ← Python dependencies

├── 📄 README\_FIRST.txt ← Quick-start guide

│

├── 📁 notebooks/ ← All 6 Jupyter Notebooks (.ipynb)

│ ├── 1\_Attendance\_System.ipynb

│ ├── 2\_Animal\_Detection.ipynb

│ ├── 3\_Drowsiness\_Detection.ipynb

│ ├── 4\_Nationality\_Detection.ipynb

│ ├── 5\_SignLanguage\_Detection.ipynb

│ └── 6\_CarColor\_Detection.ipynb

│

├── 📁 models/ ← Saved model weights (if applicable)

│ └── \*.h5 / \*.pt / \*.pb

│

└── 📁 assets/ ← Sample test media

├── images/

└── videos/

---



\## ▶️ How to Run the Projects



\### Step 1: Setup Environment

Ensure you have \*\*Python 3.8 or higher\*\* installed.



Create and activate a virtual environment (recommended):



```bash

python -m venv cv\_env

\# On Windows:

cv\_env\\Scripts\\activate

\# On macOS/Linux:

source cv\_env/bin/activate]



**Step 2: Install Dependencies**

From the root folder, run:

pip install -r requirements.txt



**Step 3: Launch Jupyter Notebook**

**jupyter notebook**



**⚙️ Dependencies (requirements.txt)**

**All required libraries are listed below. Save this as requirements.txt:**

**tensorflow>=2.10.0**

**opencv-python>=4.5.0**

**mediapipe>=0.10.0**

**scikit-learn>=1.2.0**

**pandas>=1.5.0**

**numpy>=1.21.0**

**matplotlib>=3.7.0**

**Pillow>=9.0.0**

**imutils>=0.5.4**

**tk**

**jupyter**



**🎯 Project-Specific Notes**

**1. Attendance System Model**

**Uses FaceNet + SVM for recognition, FER CNN for emotion.**

**Only activates between 9:30 AM – 10:00 AM (system time).**

**Output: attendance\_log.csv generated in project folder with timestamps.**

**No GUI — CLI/console based.**

**2. Animal Detection Model**

**Uses YOLOv5/SSD trained on custom/COCO animal dataset.**

**Carnivores highlighted in RED bounding boxes.**

**Pop-up message shows count of carnivorous animals detected.**

**GUI supports image upload + video feed + real-time preview.**

**3. Drowsiness Detection Model**

**Uses MediaPipe/Dlib facial landmarks → eye/mouth aspect ratio → binary classifier.**

**Sleeping persons marked in RED.**

**Predicts age using regression/classifier head.**

**Pop-up shows: “Sleeping: 2 people → Ages: 24, 31”**

**GUI supports image + video input with preview.**

**4. Nationality Detection Model**

**Fine-tuned ResNet/ViT for nationality classification.**

**Emotion: FER model.**

**Dress color: HSV masking + dominant color extraction.**

**Conditional output logic:**

**Indian → Age + Dress Color + Emotion**

**US → Age + Emotion**

**African → Dress Color + Emotion**

**Others → Nationality + Emotion**

**GUI includes upload button, image preview, dynamic output panel.**

**5. Sign Language Detection**

**Trained on ASL/static gesture dataset using CNN or MediaPipe Hands + LSTM.**

**Only active between 6:00 PM – 10:00 PM (system time check).**

**GUI supports:**

**Image upload → single prediction**

**Live webcam → real-time classification**

**Vocabulary: \[Specify your chosen words, e.g., “Hello”, “Thank You”, “Yes”, “No”]**

**6. Car Colour Detection Model**

**Vehicle detection: YOLOv5 or Haar Cascade.**

**Color detection: K-means clustering on ROI or dominant color via histogram.**

**Blue cars → Red rectangle**

**Other cars → Blue rectangle**

**Pedestrian count near traffic signal using pose/human detector.**

**GUI displays annotated image + counters.**

**⚠️ Troubleshooting \& Tips**

**Issue	Solution**

**GUI doesn’t open / crashes	Ensure you’re not running headless (SSH/server). Use local machine with display.**

**ModuleNotFoundError	Double-check requirements.txt and reinstall missing packages.**

**Time-based features not triggering	Ensure system clock matches expected timezone. Code uses datetime.now().time().**

**Low FPS in video processing	Reduce frame resolution, skip frames, or use lighter models (MobileNet, MediaPipe).**

**Model not detecting anything	Check confidence threshold — may be set too high. Lower it (e.g., from 0.7 → 0.4).**

**Memory overload	Clear GPU cache after each prediction: tf.keras.backend.clear\_session()**

**📌 Additional Notes**

**All notebooks include markdown headers, inline comments, and sample outputs for clarity.**

**Screenshots of GUIs, pop-ups, and detection results are embedded within notebooks.**

**CSV logs (Attendance System) and confusion matrices (where applicable) are saved locally.**

**For reproducibility, random seeds are fixed where possible.**



