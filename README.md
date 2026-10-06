# 🏭 Wafer Sensor Fault Detection

An end-to-end Machine Learning and MLOps system for real-time sensor fault detection in semiconductor wafer manufacturing processes.

---

## 📌 Project Overview
In wafer fabrication, hundreds of sensitive sensors continuously monitor equipment temperature, pressure, chemical flow, and processing times. A single malfunctioning sensor can compromise an entire batch, leading to millions of dollars in yield loss.

This project delivers a robust, production-ready ML classification pipeline to detect faulty wafers and anomalies in real-time, enabling proactive equipment maintenance and quality assurance.

---

## 🛠️ Architecture & Tech Stack

- **Machine Learning & Modeling:** Scikit-Learn, XGBoost, Random Forest, Imbalanced-Learn (SMOTE)
- **Web Application / API:** Flask (`app.py`), HTML5, CSS3, JavaScript
- **Data Ingestion & Storage:** MongoDB / Cloud Storage integration (`upload_data.py`)
- **Pipeline Architecture:** Modular MLOps pipeline structure in `src/` (Data Ingestion, Data Validation, Data Transformation, Model Trainer, Model Evaluator, Prediction Pipeline)
- **Deployment & Config:** Modular YAML configuration (`config/`), automated packaging via `setup.py`

---

## 📂 Repository Structure
```
├── config/                  # Configuration YAML files for training & prediction pipelines
├── src/                     # Core application source code
│   ├── components/          # Ingestion, validation, transformation, training, evaluation
│   ├── pipeline/            # Training pipeline and prediction pipeline orchestration
│   ├── constant/            # Environment, DB, and file system constants
│   ├── entity/              # Artifact and configuration entity classes
│   ├── exception/           # Custom exception handling
│   ├── logger/              # Centralized logging system
│   └── utils/               # Common helper utilities
├── templates/               # Flask HTML templates
├── static/                  # CSS, JavaScript, and asset files
├── app.py                   # Flask web application entrypoint
├── upload_data.py           # Script to push sensor batches to MongoDB
├── setup.py                 # Python package setup configuration
├── requirements.txt         # Project dependencies
└── README.md                # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8
- MongoDB instance (Local or MongoDB Atlas)

### Setup & Execution
1. **Clone the repository:**
   ```bash
   git clone https://github.com/lavyadav128/Wafer-Sensor-Fault-Detection.git
   cd Wafer-Sensor-Fault-Detection
   ```

2. **Create and activate a virtual environment:**
   ```bash
   conda create -n sensor python=3.8 -y
   conda activate sensor
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application:**
   ```bash
   python app.py
   ```
   Open your browser and navigate to `http://localhost:5000` to trigger model training or batch sensor predictions.

---

## 👤 Author
- **Lav Kumar Yadav**
- GitHub: [@lavyadav128](https://github.com/lavyadav128)
- LinkedIn: [Lav Kumar Yadav](https://www.linkedin.com/in/lav-yadav-90476981)