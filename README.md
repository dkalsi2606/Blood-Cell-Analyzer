# Blood Anomaly Detector & Classifier

A web-based AI-powered blood report analysis tool that detects anomalies, classifies blood cell types, and predicts potential blood-related conditions from uploaded blood report images.

## Features

* Upload blood report images (`PNG`, `JPG`, `JPEG`, `WEBP`)
* AI-powered anomaly detection
* Blood cell classification
* Disease risk estimation
* CBC parameter extraction
* Age and sex-adjusted reference ranges
* Interactive visualization dashboard
* Risk scoring system
* Responsive modern UI
* PDF report export support

---

## Project Overview

This project uses:

* **Frontend:** HTML, CSS, JavaScript
* **AI API:** Groq API
* **Image Processing:** Base64 image handling
* **Visualization:** Custom JavaScript rendering

The application analyzes uploaded blood report images and returns:

* Extracted CBC values
* Abnormality detection
* Cell type classification
* Disease prediction indicators
* Risk assessment
* Visual reference comparisons

---

## Folder Structure

```bash
blood_anomaly/
│
├── index.html                      # Main UI
├── app.js                          # File handling + API calls
├── render.js                       # Result rendering logic
├── data.js                         # Medical ranges + AI prompts
├── config.js                       # API key configuration
├── blood_anomaly.ipynb             # Research / experimentation notebook
├── blood_cell_anomaly_detection.csv
├── cell_type_reference.csv
├── report_01_normal_male.png
├── report_02_iron_deficiency_anemia.png
├── report_03_bacterial_infection_sepsis.png
├── report_04_aml_suspected.png
└── report_05_sickle_cell.png
```

---

# Screenshots / Demo Inputs

The `files/` folder contains sample blood reports for testing:

* Normal blood report
* Iron deficiency anemia
* Bacterial infection / sepsis
* AML suspected case
* Sickle cell disease

You can upload these examples directly into the application.

---

# Installation

## 1. Clone the Repository

```bash
git clone <your-repository-url>
cd blood_anomaly
```

---

## 2. Configure API Key

Open `config.js` and replace the placeholder with your Groq API key:

```javascript
const API_KEY = "YOUR_GROQ_API_KEY";
```

Get your API key from:

[https://console.groq.com/keys](https://console.groq.com/keys)

---

## 3. Run the Project

Since this is a frontend-only project, simply open:

```bash
index.html
```

Or run a local server:

### VS Code Live Server

* Install the **Live Server** extension
* Right-click `index.html`
* Click **Open with Live Server**

### Python Local Server

```bash
python -m http.server 8000
```

Then open:

```bash
http://localhost:8000
```

---

# How It Works

## Step 1 — Upload Blood Report

The user uploads a blood report image.

Supported formats:

* PNG
* JPG
* JPEG
* WEBP

Maximum file size:

* 5 MB

---

## Step 2 — AI Analysis

The application sends the image to the Groq API for analysis.

The AI model extracts:

* CBC values
* Blood cell information
* Abnormal markers
* Disease indicators

---

## Step 3 — Result Visualization

Results are displayed with:

* Risk levels
* Confidence scores
* CBC range indicators
* Disease classification
* Cell-type predictions
* CytoDiffusion anomaly score

---

# Medical Parameters Included

The project supports analysis for:

| Parameter  | Description                               |
| ---------- | ----------------------------------------- |
| WBC        | White Blood Cell Count                    |
| RBC        | Red Blood Cell Count                      |
| Hemoglobin | Hemoglobin Level                          |
| Hematocrit | Hematocrit Percentage                     |
| Platelets  | Platelet Count                            |
| MCV        | Mean Corpuscular Volume                   |
| MCHC       | Mean Corpuscular Hemoglobin Concentration |

---

# Supported Cell Types

## Normal Cells

* Neutrophil
* Lymphocyte
* Monocyte
* Eosinophil
* Basophil
* Erythrocyte
* Platelet

## Abnormal Cells

The model also detects several abnormal blood cell patterns and anomaly indicators.

---

# Risk Levels

The system categorizes reports into:

* Low Risk
* Moderate Risk
* High Risk
* Critical Risk

Using:

* CBC abnormalities
* AI anomaly confidence
* Disease prediction confidence
* CytoDiffusion scoring

---

# Example Use Cases

* Educational hematology demonstrations
* AI healthcare research
* Blood report visualization systems
* Medical AI prototypes
* CBC anomaly screening
* Academic projects

---



## Disclaimer

This project is intended for:

* Educational purposes
* Research purposes
* Prototype demonstrations

It is **NOT** a replacement for professional medical diagnosis.

Always consult certified
