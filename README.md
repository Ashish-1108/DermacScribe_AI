**Dermascribe** 
Dermascribe is an intelligent, multi-feature skincare advisor built with Python and Streamlit. It's designed to combat the confusion of the modern skincare market by providing personalized, data-driven guidance.
The Problem: Consumers often follow skincare trends blindly, risking harmful ingredient reactions and using ineffective products due to a lack of personalized, data-driven guidance.
Dermascribe addresses this by moving from "guessing" to "knowing" with a suite of powerful analytical tools.
Key Features
Our project is built on 6 core features, each running as a dedicated Streamlit application:
Product Combination Analyzer (1_Product_Analyzer.py)
Eliminate the guesswork from layering. This tool instantly cross-references every product in your routine to flag harmful ingredient combinations, ensuring your regimen is safe and effective.
AI Face-Scan Advisor (2_AI_Face_Check.py)
Go beyond generic advice. Our "FaceScan AI" provides hyper-personalized recommendations, using computer vision to analyze your skin's unique needs or by simply listening to your concerns.
RegiScore Analyzer (4_Routine_Rater)
Answer a dynamic quiz about your lifestyle, habits, and routine to receive an "Effectiveness Score." This tool provides a holistic report on what you're doing right and where you can improve.
Genetic-Skin Risk Analyzer (3_Genetic_Analyzer)
Understand your skin's predispositions. By providing basic family skin history, this tool identifies potential hereditary skin conditions, empowering you with preventative care advice.
The Ingredient Decoder (5_Glossary)
Knowledge is power. This is a comprehensive, searchable A-Z glossary for any skincare ingredient, explaining what it does, who it's for, and what it shouldn't be mixed with.
Daily UV Index Alert (6_Sunsafe_Notifier)
Your skin's daily forecast. This tool provides your location's local UV Index and sends a browser notification with tailored sunscreen advice if the UV index is high.
 Technology Stack
This project is built entirely in Python, leveraging the following libraries:
Frontend: Streamlit (with custom HTML/CSS for styling)
AI & Machine Learning: Google Gemini (google-generativeai) for recommendations and analysis.
Computer Vision: OpenCV (used in 2_AI_Face_Check.py for face analysis - implied, add to requirements if used)
Data Handling: Pandas
Data Visualization: Altair, Plotly
Web APIs: Requests (for OpenWeatherMap API)
Browser Interaction: streamlit_js_eval (for geolocation in 6_Sunsafe_Notifier)
MODULES Overview
Each feature is a standalone Streamlit app:
1_Product_Analyzer.py : Ingredient Compatibility Scanner. Manages your product list and runs conflict analysis.
2_AI_Face_Check.py: AI Powered Recommendation. Handles both image upload (face-scan) and text-based concerns to generate AI recommendations.
4_Routine_Rater: Daily Routine Analysis. A multi-step quiz that generates a score and detailed report on your habits.
3_Genetic_Analyzer: Genetic Risk Insights. A questionnaire to identify potential hereditary skin condition risks.
5_Glossary.py: Ingredient Glossary. A searchable, filterable ingredient database.
6_Sunsafe_Notifier: Weather Alerts. Fetches local weather/UV data and provides skincare tips.
Running Locally
To run this project, you can launch any of the 6 feature apps.
1. Clone the Repository
git clone [https://github.com/your-username/dermascribe.git](https://github.com/your-username/dermascribe.git)
cd dermascribe


2. Set Up a Virtual Environment
# Windows
python -m venv venv
.\venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate


3. Install Requirements
A requirements.txt file is included.
pip install -r requirements.txt

4. Make Database
Python build_database.py

5. Set Up API Keys
This project requires API keys for AI and weather data. Create a file named .streamlit/secrets.toml and add your keys:
# .streamlit/secrets.toml

GEMINI_API_KEY = "YOUR_GEMINI_API_KEY_HERE"
OPENWEATHER_API_KEY = "YOUR_OPENWEATHERMAP_API_KEY_HERE"


6. Run Your Chosen Feature
Each .py file is its own app. Run any of them using streamlit run:
# To run the AI Face-Scan Advisor
streamlit run 2_AI_Face_Check.py

# To run the Ingredient Compatibility Scanner
streamlit run 1_Product_Analyzer.py

# To run the Genetic Risk Analyzer
streamlit run 3_Genetic_Analyzer

# ...and so on for each file!


Disclaimer
This tool is for informational and educational purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment. Always consult with a qualified dermatologist for any skin concerns.
