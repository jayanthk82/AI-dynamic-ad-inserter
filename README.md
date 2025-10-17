# AI-dynamic-ad-inserter
This project, AI Dynamic Ad Inserter, is a computer vision tool designed to intelligently and automatically place advertisements onto flat surfaces within a video.

The system analyzes a video to identify suitable planes—such as walls, floors, or tabletops—and then realistically overlays a target advertisement image onto the chosen surface. It handles the complexities of perspective, ensuring the ad appears naturally integrated into the scene.

Core Technologies
This project leverages a modern stack of AI and computer vision libraries:

Python: The primary programming language.

OpenCV: Used for core video processing tasks like reading and writing frames.

PyTorch: The deep learning framework powering our AI models.

MiDaS: A state-of-the-art deep learning model for monocular depth estimation, allowing the program to "see" the 3D structure of the scene and identify surfaces.

Segment Anything Model (SAM): A powerful foundation model from Meta AI used to generate precise masks of the identified surfaces for seamless integration.

How It Works
The workflow is a multi-stage pipeline:

Surface Identification: The system processes the input video frame by frame. The MiDaS model analyzes each frame to create a depth map, identifying potential flat surfaces suitable for ad placement.

Precise Segmentation: Once a surface is targeted, the Segment Anything Model (SAM) is used to generate an exact pixel-level mask of that area.

Perspective Transformation: The system calculates the corner points of the segmented surface to understand its perspective relative to the camera. It then applies a perspective warp to the advertisement image, distorting it to perfectly match the angle and orientation of the surface in the video.

Seamless Integration: Finally, the warped advertisement is overlaid onto the video frame using the mask from SAM, resulting in a final video where the ad appears to be a natural part of the original environment.
