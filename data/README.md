# Input data

The project includes the following input files. You can replace them with your own files, keeping the names expected by the notebooks:

| File | Used in | What to capture |
|---|---|---|
| `photo1.jpeg` | Unit 3 and Unit 4 | Main image used for restoration, segmentation, and feature extraction. |
| `photo2.jpeg` | Unit 4 | Second image used for feature matching. |
| `photo5.jpeg` | Unit 5 | Image used for face and object recognition. |
| `objects.jpeg` | Unit 3 (watershed) | Image used for watershed segmentation. |
| `video.mp4` | Unit 5 | Video used for motion estimation. |

Tips:
* Do **not** edit or filter the originals.
* iPhone photos in `.HEIC` format cannot be read by OpenCV. Either convert them to `.jpg`, or set *Settings → Camera → Formats → Most Compatible* before shooting.
* If your video is `.mov`, either rename the path in the notebook (`VIDEO_PATH = "data/video.mov"`) or convert it to `.mp4`.
The supplied input files are included in the repository. The notebooks expect these exact file names and paths.
