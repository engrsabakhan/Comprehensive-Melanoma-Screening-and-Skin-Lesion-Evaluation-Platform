🩺 <span style="color:#d9534f;">Melanoma Detection – Image Processing Pipeline</span>

A professional image processing pipeline for dermatological lesion analysis and melanoma detection.

📋 Project Overview

This project implements an automated image preprocessing and segmentation workflow for skin lesion analysis using Python, OpenCV, and scikit-image.
It focuses on enhancing dermatological images, removing artifacts, and generating accurate lesion masks.

🚀 Features

Automated dermatological image preprocessing

Hair detection & removal

Noise reduction using median filtering

Threshold-based segmentation

Morphological cleaning & gap filling

RGB channel analysis + histograms

Final binary mask generation

🔬 Image Processing Pipeline
1️⃣ Color Processing

RGB channel separation

Convert to grayscale

2️⃣ Preprocessing

Median filtering (5px disk)

Hair removal using erosion (elliptical kernel)

3️⃣ Segmentation

Binary thresholding at 127

4️⃣ Morphological Operations

Opening (5×5 ellipse)

Closing (15×15 ellipse)

Dilation (5×5 ellipse)

Gap Filling (20×20 ellipse)

5️⃣ Border Cleaning

100px border removal to eliminate edge noise

6️⃣ Output Generation

Final segmented mask

RGB histograms

Intermediate visual outputs

🛠️ Technologies Used
<table style="border-collapse: collapse; width:100%;"> <tr style="background:#f2f2f2;"> <th style="padding:8px; border:1px solid #ddd;">Technology</th> <th style="padding:8px; border:1px solid #ddd;">Purpose</th> </tr> <tr> <td style="padding:8px; border:1px solid #ddd;">Python</td> <td style="padding:8px; border:1px solid #ddd;">Core programming language</td> </tr> <tr> <td style="padding:8px; border:1px solid #ddd;">OpenCV</td> <td style="padding:8px; border:1px solid #ddd;">Image processing operations</td> </tr> <tr> <td style="padding:8px; border:1px solid #ddd;">scikit-image</td> <td style="padding:8px; border:1px solid #ddd;">Segmentation & filtering tools</td> </tr> <tr> <td style="padding:8px; border:1px solid #ddd;">NumPy</td> <td style="padding:8px; border:1px solid #ddd;">Array operations</td> </tr> <tr> <td style="padding:8px; border:1px solid #ddd;">Matplotlib</td> <td style="padding:8px; border:1px solid #ddd;">Histogram visualization</td> </tr> </table>
📁 Project Structure
melanoma-detection/
│
├── DIP project.ipynb          # Main notebook
├── data/
│   ├── colored/               # Input skin images
│   └── segmented/             # Output processed masks
├── requirements.txt           # Dependencies
└── README.md                  # Documentation

⚙️ How to Use
1️⃣ Install Dependencies
pip install opencv-python scikit-image matplotlib numpy

2️⃣ Set Input & Output Paths
folder_path = r"C:\Users\PMYLS\Desktop\Data\colored"
output_folder = r"C:\Users\PMYLS\Desktop\Data\segmented"

3️⃣ Process Images
for image_file in image_files:
    image_path = os.path.join(folder_path, image_file)
    save_path = os.path.join(output_folder, f"segmented_{image_file}")
    process_image(image_path, save_path)

⚙️ Configuration Parameters
<table style="border-collapse:collapse; width:100%;"> <tr style="background:#f2f2f2;"> <th style="padding:8px; border:1px solid #ddd;">Operation</th> <th style="padding:8px; border:1px solid #ddd;">Parameter</th> </tr> <tr><td style="padding:8px; border:1px solid #ddd;">Median Filter</td><td style="padding:8px; border:1px solid #ddd;">5px disk</td></tr> <tr><td style="padding:8px; border:1px solid #ddd;">Erosion</td><td style="padding:8px; border:1px solid #ddd;">5×5 ellipse, 2 iterations</td></tr> <tr><td style="padding:8px; border:1px solid #ddd;">Threshold</td><td style="padding:8px; border:1px solid #ddd;">127</td></tr> <tr><td style="padding:8px; border:1px solid #ddd;">Opening</td><td style="padding:8px; border:1px solid #ddd;">5×5 ellipse</td></tr> <tr><td style="padding:8px; border:1px solid #ddd;">Closing</td><td style="padding:8px; border:1px solid #ddd;">15×15 ellipse</td></tr> <tr><td style="padding:8px; border:1px solid #ddd;">Dilation</td><td style="padding:8px; border:1px solid #ddd;">5×5 ellipse</td></tr> <tr><td style="padding:8px; border:1px solid #ddd;">Gap Filling</td><td style="padding:8px; border:1px solid #ddd;">20×20 ellipse</td></tr> <tr><td style="padding:8px; border:1px solid #ddd;">Border Mask</td><td style="padding:8px; border:1px solid #ddd;">100px</td></tr> </table>
⚠️ Medical Disclaimer

This project is for research and educational purposes only.
Not for clinical use. Consult a dermatologist for medical concerns.

🤝 Contributing

Improve segmentation accuracy

Add more morphological techniques

Enhance visualization

Improve processing speed
