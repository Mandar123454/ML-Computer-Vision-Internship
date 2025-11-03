# CarColor_Detection models

Suggested artifacts:
- yolov5s.pt (or other detector weights: ONNX/TFLite)
- class_names.txt (COCO class names if using COCO-trained detector)

Notes:
- The notebook currently mocks YOLO detections. Replace with real detector weights and inference code, then place weights here.
- If using Ultralytics YOLOv5/8, keep a note of version used to avoid API drift.