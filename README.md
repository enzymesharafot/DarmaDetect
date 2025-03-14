# DarmaDetect

## 🩺 AI-Powered Skin-Disease Detection System
DarmaDetect is a deep learning-based system designed to detect skin-disease from skin images. It leverages a **DenseNet201** model trained on a medical dataset to classify images into **BA- cellulitis, BA-impetigo, FU-athlete-foot, FU-nail-fungus, FU-ringworm, PA-cutaneous-larva-migrans, VI-chickenpox and VI-shingles** categories. The system consists of:
- **Backend**: FastAPI-based RESTful API for image processing and model inference.
- **Frontend**: A user-friendly interface (HTML/JS) for uploading and analyzing skin images.
- **Model**: A pre-trained Deep Learning model (DenseNet201) for accurate disease classification.

## ✨ Features
- ✅ **Upload skin images** for real-time skin-disease analysis.
- ✅ **Deep learning-based classification** (BA- cellulitis, BA-impetigo, FU-athlete-foot, FU-nail-fungus, FU-ringworm, PA-cutaneous-larva-migrans, VI-chickenpox, VI-shingles).
- ✅ **FastAPI-powered backend** for quick inference.
- ✅ **Interactive frontend** for seamless user experience.
- ✅ **API documentation** via FastAPI's built-in `/docs` endpoint.

---

## 🛠️ Tech Stack
- **Backend**: FastAPI, Python, PyTorch, Uvicorn
- **Frontend**: HTML, CSS, JS
- **Model**: DenseNet201 (pre-trained on medical datasets)
- **Data Handling**: NumPy, Pillow,

---

## ⚡ Installation & Usage

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/enzymesharafot/DarmaDetect
cd darmadetect
```

### 2️⃣ Backend Setup
#### **Install Dependencies**
```bash
cd backend
python -m venv venv  # Create a virtual environment
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirement.txt  # Install dependencies
```

#### **Run FastAPI Server**
```bash
uvicorn main:app --reload
```
- The API will be available at **http://127.0.0.1:8000**.
- Interactive API documentation: **http://127.0.0.1:8000/docs**.

### 3️⃣ Frontend Setup
If using a simple **HTML/JS frontend**, just open `index.html` in a browser.

---

## 🌐 API Endpoints
| Method | Endpoint    | Description |
|--------|------------|-------------|
| `POST` | `/prediction/` | Uploads an eye image and returns the disease classification. |
| `GET`  | `/docs`    | Access the FastAPI interactive documentation. |

#### **Example API Request** (Using `curl`)
```bash
curl -X POST "http://127.0.0.1:8000/predict" -F "file=@sample_image.jpg"
```
#### **Response Format**
```json
{
  "prediction": "BA-impetigo"
}
```

---

## 🧠 Model Details
- **Architecture**: DenseNet201
- **Input Shape**: (224, 224, 3)
- **Output Classes**: BA- cellulitis, BA-impetigo, FU-athlete-foot, FU-nail-fungus, FU-ringworm, PA-cutaneous-larva-migrans, VI-chickenpox, VI-shingles
- **Dataset**: Trained on `subirbiswas19/skin-disease-dataset`
- **Accuracy**: 94.1302% on test data

---

## 🏆 Features & Roadmap
- **Current Features**:
  - Upload and analyze skin-disease images.
  - Detect potential diease using AI.
  
- **Planned Features**:
  - Optimize the model with **OpenVINO** or **TensorRT** for real-time inference.
  - Add support for mobile device image uploads.
  - Extend classification to other skin diseases.

---

## 🚀 Future Enhancements
- Add **multi-class classification** for different skin diseases.
- Implement **real-time video processing**.
- Improve model accuracy with additional datasets & augmentations.
- **Integration with Kubeflow Pipelines** for scalable training and inference.
- **Cloud Deployment**: AWS Lambda / GCP Cloud Run / Azure ML.

---

## 📜 License
This project is licensed under the **MIT License**.

---

## 💡 Acknowledgments
- Inspiration: *Deep Learning for Medical Imaging*
- Open-source libraries: PyTorch, FastAPI, OpenCV

### 🚀 Get Started Now! Build the future of AI-powered healthcare with DarmaDetect. 😎
