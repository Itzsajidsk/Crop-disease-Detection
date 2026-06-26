# Crop Disease Detection 🌿

An AI-powered application designed to detect crop diseases from plant leaf images. This project provides an accessible and scalable way for farmers and agricultural enthusiasts to quickly identify health issues in their plants by simply uploading a photo.

## 🚀 How It Works

1. **Upload an Image**: The user uploads an image of a plant leaf using the modern React-based web interface.
2. **Preprocessing**: The frontend sends the image to the FastAPI backend, which preprocesses the image to match the requirements of the machine learning model.
3. **Inference**: The backend runs the image through an advanced deep learning model. The system supports a flexible adapter pattern to easily swap between ONNX, TensorFlow, and PyTorch models.
4. **Prediction**: The model returns the predicted disease class along with a confidence score.
5. **Results**: The frontend displays the diagnosis to the user, letting them know if the plant is healthy or infected, and what specific disease it might be.

## 🛠️ Technology Stack

- **Frontend**: React, TypeScript, Vite, Tailwind CSS
- **Backend**: FastAPI (Python), Uvicorn
- **Machine Learning**: Support for TensorFlow, PyTorch, and ONNX models
- **Testing & Performance**: Pytest, Locust

## 🍅 Supported Crops & Diseases

The model is trained to recognize a wide variety of plant species and their corresponding diseases, including:

- **Apple**: Scab, Black Rot, Cedar Apple Rust, Healthy
- **Corn (Maize)**: Cercospora Leaf Spot, Common Rust, Northern Leaf Blight, Healthy
- **Grape**: Black Rot, Esca (Black Measles), Leaf Blight, Healthy
- **Potato**: Early Blight, Late Blight, Healthy
- **Tomato**: Bacterial Spot, Early/Late Blight, Leaf Mold, Septoria Leaf Spot, Spider Mites, Target Spot, Yellow Leaf Curl Virus, Mosaic Virus, Healthy
- **Other Crops**: Mango (Anthracnose), Citrus (Canker), Rice (Blast), Wheat (Rust)

## 💻 Getting Started

### Prerequisites
- Node.js (v18+)
- Python 3.9+

### Backend Setup
1. Navigate to the `backend` directory:
   ```bash
   cd backend
   ```
2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   # On Windows:
   .\venv\Scripts\activate
   # On Mac/Linux:
   source venv/bin/activate
   ```
3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the API server:
   ```bash
   uvicorn app.main:app --reload
   ```
   *The backend will be running at `http://localhost:8000`*

### Frontend Setup
1. Navigate to the `frontend` directory:
   ```bash
   cd frontend
   ```
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```
   *The frontend will be available at `http://localhost:5173` (or the port specified by Vite)*

## 🤝 Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request if you'd like to improve the models, add new crops, or enhance the user interface.
