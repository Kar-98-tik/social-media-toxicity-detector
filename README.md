# Social Media Toxicity Detector

This repository contains a **Social Media Toxicity Detector** that uses the [DistilBERT](https://huggingface.co/distilbert-base-uncased) tokenizer and the [unitary/toxic-bert](https://huggingface.co/unitary/toxic-bert) model to predict the toxicity of user comments. The tool provides both numerical toxicity scores and a graphical comparison of toxicity categories.

---

## 🚀 Features
- Predicts the probability of the following toxicity categories:
  - Toxic
  - Severe Toxic
  - Obscene
  - Threat
  - Insult
  - Identity Hate
- Provides an easy-to-read comparison bar graph of the toxicity scores.
- Simple to use and extend.

---

## 🛠️ Installation
1. **Clone the repository:**
```bash
git clone https://github.com/kar98tik/social-media-toxicity-detector.git
cd social-media-toxicity-detector
```

2. **Create a virtual environment (optional but recommended):**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install the required dependencies:**
```bash
pip install -r requirements.txt
```

> **Note:** The requirements file includes:
> - `transformers`
> - `torch`
> - `matplotlib`

---

## 📈 Usage
1. **Run the script:**
```bash
python toxicity_detector.py
```

2. **Example code snippet:**
```python
from toxicity_detector import predict_toxicity

comment = "You are an idiot!"
result = predict_toxicity(comment)
print(result)  # Prints toxicity scores
toxicity_graph(result)  # Displays comparison graph
```

---

## 📊 Output Example
For the comment: `"You are an idiot!"`, you will get output like:
```json
{
  "toxic": 0.95,
  "severe_toxic": 0.65,
  "obscene": 0.85,
  "threat": 0.10,
  "insult": 0.90,
  "identity_hate": 0.05
}
```

And a bar graph comparing the scores:
- Higher bars represent higher toxicity probabilities in that category.

---

## 📂 Project Structure
```
social-media-toxicity-detector/
├── toxicity_detector.py      # Main code for toxicity detection
├── requirements.txt          # Required dependencies
└── README.md                 # Project documentation
```

---

## 🧪 Testing
- Add various comments in `toxicity_detector.py` to test different toxicity levels.
- Modify the text input and observe the graph and score changes.

---

## 📢 Contributing
Pull requests are welcome! If you find bugs or have feature suggestions, please open an issue or submit a PR.

---

## 📝 License
This project is open-source and available under the MIT License.

---

## 👨‍💻 Author
Developed by **Kartik (kar98tik)** 🚀
