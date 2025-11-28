# Heart Attack Predictor

A Streamlit-based machine learning application that predicts the risk of heart disease using a Random Forest classifier.

## Features

- **Single Prediction**: Input individual health metrics to get instant heart attack risk assessment
- **Batch Predictions**: Process multiple records from CSV files
- **Model Training**: Train a new Random Forest model from data if needed
- **Interactive UI**: User-friendly Streamlit interface with real-time predictions

## Project Structure

```
heartattack/
├── app.py                 # Main Streamlit application
├── Heart_attack.csv       # Training/prediction dataset
├── rfc.jb                 # Pre-trained Random Forest model (joblib format)
├── requirements.txt       # Python dependencies
├── .gitignore            # Git ignore patterns
└── README.md             # This file
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/nikhilyadav/heartattack.git
cd heartattack
```

2. Create a virtual environment:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Run the Streamlit app:
```bash
streamlit run app.py
```

The application will open at `http://localhost:8501`

### Input Features

- **HighBP**: High blood pressure (0/1)
- **HighChol**: High cholesterol (0/1)
- **CholCheck**: Cholesterol check (0/1)
- **BMI**: Body Mass Index (numeric)
- **Smoker**: Smoking status (0/1)
- **Stroke**: History of stroke (0/1)
- **Diabetes**: Diabetes status (0/1)
- **PhysActivity**: Physical activity (0/1)
- **HvyAlcoholConsump**: Heavy alcohol consumption (0/1)
- **MentHlth**: Mental health days (0-30)
- **PhysHlth**: Physical health days (0-30)
- **Sex**: Gender (0=Female, 1=Male)
- **Age**: Age category (numeric)
- **Education**: Education level (numeric)
- **Income**: Income level (numeric)

## Model Information

- **Algorithm**: Random Forest Classifier (200 estimators)
- **Training Accuracy**: ~89%
- **Features**: 15 health and demographic indicators

## Dataset

The `Heart_attack.csv` file should contain the following columns:
- All 15 features listed above
- `target`: Binary target variable (0=no heart attack risk, 1=heart attack risk)

## Configuration

Before running, edit the following paths in `app.py` if needed:
```python
DEFAULT_MODEL_PATH = "/path/to/your/rfc.jb"
DEFAULT_DATA_PATH = "/path/to/your/Heart_attack.csv"
```

## Requirements

- Python 3.7+
- streamlit
- pandas
- scikit-learn
- numpy
- joblib

## License

MIT License

## Author

Nikhil Yadav
