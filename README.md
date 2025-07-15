# LipNet (TensorFlow, Apple Silicon/MPS)

This project implements LipNet, a deep learning model for lip reading, using TensorFlow and is optimized to run on Apple Silicon (M1/M2/M3) Macs with Metal Performance Shaders (MPS) acceleration.

## Features
- Loads and preprocesses video data for lip reading
- Builds and trains a deep neural network for sequence prediction
- Supports GPU acceleration via MPS on Apple Silicon

## Requirements
- macOS with Apple Silicon (M1/M2/M3 recommended)
- Python 3.8–3.12
- [Homebrew](https://brew.sh/) (recommended for installing ffmpeg if needed)

## Installation

1. **Clone the repository**
   ```sh
   git clone <your-repo-url>
   cd LipNet
   ```

2. **(Recommended) Create a virtual environment**
   ```sh
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```
   If you don't have a `requirements.txt`, install manually:
   ```sh
   pip install tensorflow-macos tensorflow-metal opencv-python numpy matplotlib imageio gdown
   ```

4. **(Optional) Install ffmpeg**
   Some video operations may require ffmpeg:
   ```sh
   brew install ffmpeg
   ```

## Usage

1. **Download and extract the dataset**
   The script will automatically download and extract the required dataset using `gdown`.

2. **Run the script**
   ```sh
   python /Users/apple/Downloads/lipnet.py
   ```
   or, if you are in the project directory:
   ```sh
   python lipnet.py
   ```

3. **Check for MPS/Apple GPU support**
   The script will print whether it is using GPU, MPS, or CPU.

## Troubleshooting
- If you see `ModuleNotFoundError`, ensure you are using the correct Python environment where all packages are installed.
- If you have issues with video processing, ensure `ffmpeg` is installed and accessible.
- For best performance, use the latest macOS and Apple Silicon hardware.

## References
- [Original LipNet Paper](https://arxiv.org/abs/1611.01599)
- [TensorFlow-Macos](https://developer.apple.com/metal/tensorflow-plugin/)

## License
This project is for research and educational purposes only. 