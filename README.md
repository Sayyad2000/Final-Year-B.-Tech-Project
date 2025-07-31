# Face Matching Project

A B.Tech final-year project to detect and compare faces using AWS Rekognition and Python, integrated with a Streamlit interface.

## 🚀 Overview

This project implements a face verification pipeline that:

* Uploads or captures images
* Invokes AWS Rekognition’s `compare_faces` API
* Displays similarity results via a Streamlit web interface

It's designed for use cases such as attendance tracking, identity verification, or security authentication.

---

## 🧠 Key Features

* **Face comparison** using high-accuracy AWS Rekognition API
* **Streamlit-powered UI** for image upload and real-time feedback
* **Logging and feedback** for similarity metrics and match status
* **Simple architecture** for easy deployment (cloud or local)

---

## 📁 Project Structure

```
.
├── app.py                  # Main Streamlit application
├── requirements.txt       # Python dependencies
├── aws_config.py          # AWS client setup and credentials
├── utilities/
│   ├── image_utils.py     # Image loading and preprocessing functions
│   └── rekog_utils.py     # Functions for AWS Rekognition API calls
└── README.md              # Project overview and instructions
```

---

## 💠 Setup Instructions

### Prerequisites

* Python 3.7+ installed
* AWS credentials configured (via `~/.aws/credentials`, environment vars, or IAM role)
* An AWS Rekognition–enabled region

### Installation

```bash
git clone https://github.com/Sayyad2000/Final-Year-B.-Tech-Project.git
cd Final-Year-B.-Tech-Project

# (Optional) Create and activate virtual environment
python -m venv venv
venv\Scripts\activate        # Windows
# or
source venv/bin/activate     # Linux/macOS

pip install -r requirements.txt
```

---

## ⚙️ Running the Application

```bash
python -m streamlit run app.py
```

**OR**, if `streamlit` isn't globally recognized:

```bash
python -m streamlit run app.py
```

Visit `http://localhost:8501` to use the interface. Upload two images to compare – the app will display AWS Rekognition’s similarity score and match result.

---

## 📆 Configuration Options

* **Similarity threshold**: Adjustable (default: 80%) — controls match sensitivity
* **Image formats**: Supports JPEG, PNG, etc. via preprocessed byte encoding
* **Error handling**: Gracefully handles missing AWS configs or corrupt images

---

## 🧰 How It Works

1. User uploads two images via Streamlit UI
2. Images are read and converted to byte arrays
3. The application sends these to Rekognition's `compare_faces` operation
4. The response containing similarity score is rendered on the UI
5. Errors (e.g. rate limits, invalid credentials) are caught and displayed

---

## 📋 Example Usage

```
Source Image: image1.jpg  
Target Image: image2.jpg  
SimilarityThreshold: 80  

Result:
✔️ Matched! Similarity: 89.5%
```

---

## 👥 Contribution & Feedback

Feel free to fork the repo and contribute features such as:

* Real-time webcam comparison
* Batch processing of multiple faces
* Integration with a face database
* Improved error logging and UI feedback

For queries or collaboration, reach out via GitHub issues or pull requests.

---

## 🎓 License

This project is for educational purposes. If you reuse any parts, please cite appropriately.

---

### 📌 Acknowledgments

Inspired by AWS Rekognition documentation, Streamlit UI samples, and various open-source face recognition applications ([reddit.com](https://www.reddit.com/r/learnpython/comments/1h1o3tb/i_need_help_with_my_final_project_about_facial/?utm_source=chatgpt.com), [github.com](https://github.com/Vatshayan/Face-recognition-Attendance-System-Project?utm_source=chatgpt.com)).
