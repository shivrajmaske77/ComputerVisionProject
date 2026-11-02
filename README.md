# Computer Vision Practical Assignment (Units 3, 4 and 5)

**Student:** Shivraj Maske · **PRN:** 1272250999

This project covers image restoration, segmentation, feature extraction, object recognition, and motion estimation using Python, OpenCV, and YOLOv8.

## Project files

| File | Unit / task | Techniques |
|---|---|---|
| [Unit3_Restoration_Segmentation_executed.ipynb](Unit3_Restoration_Segmentation_executed.ipynb) | Unit 3 – Task 1 | Image noise and filtering, PSNR/SSIM, thresholding, morphology, Canny edges, watershed |
| [Unit4_Feature_Extraction_executed.ipynb](Unit4_Feature_Extraction_executed.ipynb) | Unit 4 – Task 2 | HOG, SIFT, descriptor matching, Lowe's ratio test, RANSAC |
| [Unit5_Recognition_Motion_executed.ipynb](Unit5_Recognition_Motion_executed.ipynb) | Unit 5 – Tasks 3 and 4 | Haar cascades, YOLOv8, failure-case tests, frame differencing, GMM background subtraction, Lucas–Kanade optical flow |
| [1272250999_ShivrajMaske_Report.pdf](1272250999_ShivrajMaske_Report.pdf) | Assignment report | Results, comparisons, explanations, and conclusions |
| [requirements.txt](requirements.txt) | Dependencies | Python packages required to run the notebooks |

## Folder structure

```
.
├── data/                       input photos and video
├── outputs/                    generated images and motion comparison video
├── Unit3_Restoration_Segmentation_executed.ipynb
├── Unit4_Feature_Extraction_executed.ipynb
├── Unit5_Recognition_Motion_executed.ipynb
├── 1272250999_ShivrajMaske_Report.pdf
├── requirements.txt
└── README.md
```

The supplied input images and `data/video.mp4` are included in this repository. See [data/README.md](data/README.md) for input-file details. The notebooks write generated results to `outputs/unit3`, `outputs/unit4`, and `outputs/unit5`.

## Setup

Requires **Python 3.10 or newer**.

```bash
python -m venv .venv
.venv\Scripts\activate          # Windows
# source .venv/bin/activate     # macOS / Linux
pip install -r requirements.txt
```

## Running

Open the project folder in VS Code and select the `.venv` kernel, or start Jupyter:

```bash
jupyter notebook
```

Open each notebook and run **Kernel → Restart & Run All**. The notebooks are independent and can be run in any order.

The first run of Unit 5 downloads the pretrained `yolov8n.pt` model (about 6 MB), so it needs an internet connection once. The model file is excluded from Git because it is downloaded automatically.

## Troubleshooting

| Problem | Fix |
|---|---|
| `FileNotFoundError` for an input image | Check that the input files are present in `data/` and their names match the paths in the notebook. |
| `Could not read data/video.mp4` | Check that `data/video.mp4` exists and is readable. |
| `module 'cv2' has no attribute 'CascadeClassifier'` | Use OpenCV 4.x; `requirements.txt` excludes OpenCV 5. |
| Watershed does not separate objects | Use an image of touching objects on a plain background, or adjust `FG_RATIO` in Unit 3. |
| Optical-flow arrows are tiny | Adjust `T` in Unit 5 to select a point where the object moves faster. |
