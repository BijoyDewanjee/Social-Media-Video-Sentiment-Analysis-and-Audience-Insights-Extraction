# Social Media Video Sentiment Analysis and Audience Insights Extraction

## Overview

This project is a machine learning-based system designed to analyze audience sentiment from social media video data and extract meaningful insights. It processes user-generated content such as comments and classifies sentiment into categories like positive, negative, or neutral.

The system includes a production-ready API built with FastAPI and supports scalable deployment using AWS. It also integrates DVC for reproducible machine learning pipelines.

## Features

- Sentiment analysis on social media comments
- Audience insights extraction
- Batch prediction support
- REST API for real-time inference
- ML pipeline tracking using DVC
- Cloud deployment readiness (AWS)

## Tech Stack

- Python
- Scikit-learn, Pandas, NumPy
- NLTK / SpaCy
- FastAPI
- DVC (Data Version Control)
- AWS (EC2, S3)

## How to Run

1. Create Virtual Environment

   ```
   conda create -n sentiment python=3.11 -y
   ```
2. Activate Environment

   ```
   conda activate sentiment
   ```
3. Install Dependencies

```
pip install -r requirements.txt
```

## DVC Pipeline

Initialize DVC

```
dvc init
```

Run pipeline

```
dvc repro
```

Visualize pipeline

```
dvc dag
```

## Running the Application

```
uvicorn api.main:app --host 0.0.0.0 --port 5000 --reload
```

API will be available at:

```
http://localhost:5000
```

## API Usage

Endpoint:
POST /predict

Sample Request:

```
{
  "comments": [
    "This video is awesome! I loved it a lot",
    "Very bad explanation, poor video"
  ]
}
```

```
Sample Response:
{
  "predictions": ["Positive", "Negative"]
}
```

## API Testing (Postman)

Send POST request to:

```
http://localhost:5000/predict
```

## AWS Setup

Configure AWS CLI

```
aws configure
```

Services used:

- EC2 for backend deployment
- S3 for storing models and data

## YouTube API Setup (GCP)

To collect video data, generate a YouTube API key from Google Cloud Platform.

Reference:

```
https://www.youtube.com/watch?v=i_FdiQMwKiw
```

## Project Structure

project-root/
│
├── data/                # Dataset files
├── src/                 # Source code
├── api/                 # FastAPI application
├── models/              # Trained models
├── notebooks/           # Experiments and analysis
├── outputs/             # Results and visualizations
├── dvc.yaml             # DVC pipeline
├── requirements.txt
└── README.md

## Results

- Successfully classifies sentiment from social media comments
- Extracts audience insights for better understanding of engagement
- Provides scalable API for real-time predictions

## Future Improvements

- Real-time sentiment streaming
- Multimodal analysis (text, audio, video)
- Transformer-based models (BERT, RoBERTa)
- Dashboard for visualization

## License

This project is licensed under the MIT License.

## Author

**Bijoy Dewanjee**
GitHub: https://github.com/BijoyDewanjee
LinkedIn: https://www.linkedin.com/in/bijoy-dewanjee-01ba621b9/
