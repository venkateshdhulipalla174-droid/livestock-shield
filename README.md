# 🐄 Smart Livestock Health Monitoring System (Livestock Shield)

An ML-powered livestock health monitoring prototype that analyzes cattle vitals to predict diseases and dispatches automated, multi-lingual alerts via SMS, WhatsApp, and Voice calls.

> **🤖 Development & AI Acknowledgment**
> The core conceptualization and system design of this project are entirely original and driven by independent research. This includes the architecture for multi-lingual alerts, the strategic selection of low-cost hardware components, and the logic for targeted physical alert mechanisms (such as severity-based buzzer and LED triggers for specific cattle). 
> 
> Artificial Intelligence tools were utilized strictly for technical execution, specifically to assist in building the Machine Learning model and writing the implementation code for API integrations.

## 🚀 Key Features

* **Machine Learning Diagnostics:** Uses a Random Forest Classifier to analyze body temperature, heart rate, physical activity (accelerometer data), and seasonal context to predict conditions like Severe Fever, Respiratory Infection, and Lameness.
* **Targeted Hardware Triggers:** Features severity-based physical alerts (LED/Buzzer triggers) on specific cattle collars, utilizing carefully researched low-cost hardware components like SIM800L GSM modules.
* **Farmer-Friendly Care Engine:** Automatically generates actionable, medically-accurate care instructions, dietary recommendations, and seasonal advice based on the predicted condition.
* **Multi-Channel Alert Dispatch:** Integrates with Twilio to instantly send SMS and WhatsApp alerts to the farmer's mobile device when anomalies are detected.
* **HD Neural Voice Calls:** Utilizes Sarvam AI and Edge-TTS to generate realistic text-to-speech audio alerts in regional languages (Hindi, Telugu, Tamil, Kannada, Marathi) and delivers them directly via automated phone calls.

## 🛠️ Tech Stack

* **Language:** Python
* **Machine Learning:** Scikit-Learn, Pandas, NumPy
* **APIs & Integrations:** Twilio API (Voice/SMS/WhatsApp), Sarvam AI API
* **Audio Processing:** Edge-TTS, gTTS, IPython Audio
* **Environment:** Google Colab

## 📊 Dataset & Model Performance
The model was trained on a Kaggle cattle dataset featuring 178 detailed records of cattle vitals. It is important to note that **the dataset size is highly limited and exhibits significant class imbalance**, with the vast majority of records representing healthy cattle. Consequently, the model's ability to generalize to a broader, real-world population is constrained. Further data collection across diverse, real-world health conditions is necessary to achieve robust predictive reliability.

## 💻 How to Run

1. Open the `IDP_proto (1).ipynb` file in Google Colab.
2. Ensure you have the required API keys (Twilio SID/Auth Token, Sarvam API Key) configured in the dispatch engine cell.
3. Run all cells to install dependencies, train the model, and launch the interactive simulation loop.
