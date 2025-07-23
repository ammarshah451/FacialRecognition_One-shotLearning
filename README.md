# FacialRecognition_One-shotLearning
Facial Recognition through one-shot learning using transfer learning




# 🚀 Facial Recognition via One-Shot Learning

This project implements a face recognition system using the `InsightFace` library and a one-shot learning approach. It detects and identifies known actors in group photos by comparing their facial embeddings with a single reference image per person.

---

## 📁 Folder Structure

Your project should be structured like this in **Colab or locally**:

project/
├── db/
│ ├── Chris_Evans.jpg
│ ├── Scarlett_Johansson.jpg
│ └── ... # One image per actor initially
│
├── group_photos/
│ ├── avengers.jpg
│ └── img2.jpg # Group test photos
│
└── facial_recognition.ipynb



------------------------------
After running, the code will auto-augment and restructure `db/` like this:


db/
├── Chris_Evans/
│   ├── Chris_Evans_orig.jpg
│   ├── Chris_Evans_aug1.jpg
│   └── ...
├── Scarlett_Johansson/
└── ...


-------------------------------


**🧠 Requirements**
Install the necessary dependencies in Google Colab:

Command:
------
!pip install insightface onnxruntime
------
The code also uses:
cv2 (OpenCV)
Pillow
torchvision
sklearn
numpy

Most are pre-installed in Colab.



---------------------

**How to Use**
*Upload your reference actor images to /db/     (take reference from structure above)
*Upload your test group photos to /group_photos/    (take reference from structure above)
*Run the notebook cell-by-cell in order

The model:
*Augments your reference images
*Extracts embeddings
*Detects faces in group photos
*Compares via cosine similarity
*Annotates predictions + calculates precision, recall, F1






