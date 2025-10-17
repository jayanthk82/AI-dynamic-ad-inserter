# AI Dynamic Ad Inserter 🤖

A computer vision tool that intelligently identifies flat surfaces in videos and seamlessly overlays advertisements with correct perspective warping.



---

## 📋 Project Description

This project leverages state-of-the-art AI models to automate the process of placing advertisements into video content. The system analyzes video frames to find suitable planes (like walls, floors, or tables), generates a precise mask for the selected area, and then realistically integrates a target ad image, handling all necessary perspective transformations.

---

## ✨ Key Features

-   **Automatic Surface Detection**: Uses depth estimation to find potential flat surfaces for ad placement.
-   **Precise Object Segmentation**: Employs the Segment Anything Model (SAM) to create accurate masks of target surfaces.
-   **Perspective Correction**: Calculates and applies a homography transformation to warp the ad image, making it fit naturally into the scene's perspective.
-   **Modular and Scalable**: Built with a clean project structure that separates concerns for easy maintenance and future development.

---

## 🛠️ Tech Stack

-   **Python 3.10**: The core programming language.
-   **OpenCV**: For fundamental video I/O and image processing tasks.
-   **PyTorch**: The deep learning framework for running the AI models.
-   **MiDaS**: A state-of-the-art model for monocular depth estimation.
-   **Segment Anything Model (SAM)**: A powerful foundation model from Meta AI for high-quality object segmentation.
-   **Conda**: For robust and reproducible environment management.
-   **Git**: For version control.

---

## 🚀 Setup and Installation

Follow these steps to set up the project environment.

**1. Clone the repository:**
```bash
git clone [https://github.com/jayanthk82/AI-dynamic-ad-inserter.git](https://github.com/jayanthk82/AI-dynamic-ad-inserter.git)
cd AI-dynamic-ad-inserter



📂 Project Structure
The project follows a standardized structure to ensure maintainability.

├── data/             # Input and Output video/image files
├── models/           # Downloaded pre-trained model weights
├── notebooks/        # Jupyter notebooks for experimentation
├── scripts/          # Core Python source code
├── tests/            # Automated tests
├── .gitignore        # Files to be ignored by Git
└── README.md         # Project documentation