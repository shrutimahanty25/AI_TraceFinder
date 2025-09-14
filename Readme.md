# ✍ Forgery Dataset Feature Extractor

A **Streamlit-based application** to automatically detect classes and extract features from forged handwritten document datasets.  
It scans the dataset folder structure, extracts statistical and visual features, and saves them into a CSV file for further analysis.

---

## 📌 Features
- Auto-detect dataset classes and sub-classes (resolutions like 150, 300).
- Extract image features:
  - Dimensions (width, height, aspect ratio, file size).
  - Intensity statistics (mean, std, skewness, kurtosis).
  - Shannon entropy.
  - Edge density (via Canny edge detection).
- Generate and save a **metadata_features.csv** file with extracted features.
- Visualize **class distribution** with bar charts.
- Preview **sample images**.

---

## 📂 Project Structure
ForgeryFeatureExtractor/
│── app.py # Main Streamlit app
│── requirements.txt # Dependencies
│── README.md # Documentation
│── venv/ (optional) # Virtual environment


---

## ⚙️ Installation & Setup

### 1️⃣ Clone or Download
Download or clone the project into your system:
```bash
git clone https://github.com/yourusername/ForgeryFeatureExtractor.git
cd ForgeryFeatureExtractor
```

### 2️⃣ Create Virtual Environment
# Windows (Command Prompt)
python -m venv venv
venv\Scripts\activate.bat

# Linux / macOS
python3 -m venv venv
source venv/bin/activate

###3️⃣ Install Requirements
pip install -r requirements.txt

###4️⃣ Run the App
streamlit run app.py

## 🖼️ Usage Instructions

Launch the app (streamlit run app.py).
Enter the dataset root path (the folder where your dataset is stored).
Expected folder structure:

dataset_root/
├── ClassA/
│   ├── 150/   # images
│   ├── 300/   # images
├── ClassB/
    ├── 150/   # images
    ├── 300/   # images


The app will:
Scan all classes and resolutions.
Extract features from each image.
Save results into metadata_features.csv inside the dataset root.
Display statistics and class distributions.



