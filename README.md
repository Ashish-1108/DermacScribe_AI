DermScribe (AI-Powered Skin Health & Genetics Platform)

“Pocket dermatologist” for personalised skincare insight and routine management

Overview

DermScribe is an intelligent, multi-feature skincare advisor built with Python and Streamlit. As described in the repository, the app addresses the modern skincare problem: consumers often follow trends blindly, risk harmful ingredient combinations, or use ineffective products due to lack of personalised data-driven guidance.

GitHub

DermScribe moves from “guessing” to “knowing” by providing a suite of analytical tools. These include:

Ingredient compatibility & product-combination checking

AI-powered face-scan or concern-based recommendation

Genetic predisposition / family-history risk insights

Routine assessment & scoring

Ingredient glossary/decoder

UV index alert & sunscreen-advice notifier

Key Features

The repository’s README lists six core features, each implemented as a dedicated Streamlit app script. 
GitHub

Below is a summary:

Feature #	Script File	Purpose
1	1_Product_Analyzer.py	Ingredient Compatibility Scanner: allows user to input a product list and checks for harmful/incompatible combinations among the ingredients. 
GitHub

2	2_AI_Face_Check.py	AI Face-Scan Advisor: user can upload a face image (or provide text concerns) and receive hyper-personalised recommendations. 
GitHub

3	3_Genetic_Analyzer.py	Genetic-Skin Risk Analyzer: based on basic family skin history, identifies potential hereditary skin condition risks and gives proactive advice. 
GitHub

4	4_Routine_Rater.py (or similar)	Routine / RegiScore Analyzer: a dynamic quiz about user’s lifestyle, habits and skincare routine, producing an “Effectiveness Score” and a report. 
GitHub

5	5_Glossary.py	Ingredient Decoder / Glossary: searchable A-Z database of skincare ingredients, telling what they do, who they’re for and what they shouldn’t be mixed with. 
GitHub

6	6_Sunsafe_Notifier.py	Daily UV Index Alert: uses weather/UV APIs to fetch local UV Index, then sends a browser notification with sunscreen advice if UV is high. 
GitHub
Technology Stack

According to the repository description, the following major technologies are used: 
GitHub

Frontend / UI: Streamlit (with custom HTML/CSS for styling)

AI & ML: e.g., Google Gemini (via google-generativeai) for recommendations and analysis

Computer Vision: OpenCV (implied for face processing)

Data Handling: Pandas

Visualization: Altair, Plotly

Web/API integration: Requests (for e.g., OpenWeatherMap API)

Browser interaction / geolocation: streamlit_js_eval (for the UV notifier geolocation)

Repository Structure

From the root of the repository (based on the repository listing): 
GitHub

/ (root)
├── Home_Dark.py
├── Home_Light.py
├── README.md
├── home1.jpg
├── home2.webp
├── home3.png
├── products.db
├── requirements.txt
├── pages/      (folder)
│     └── … (likely other supporting modules/pages)
├── test/       (folder)
└── … (the six feature scripts described above)


Notes:

There are two “home” scripts: Home_Dark.py and Home_Light.py — likely alternate themes for UI.

The products.db likely contains the ingredient/product database used by the analyzer.

The pages/ folder likely houses secondary UI pages or the Streamlit multi-page app structure.

The test/ folder suggests there are test files (unit tests or simple UI checks) though details may vary.

Setup & Running Locally

Here are the basic steps to get the project up and running (based on the repo’s README snippet). 
GitHub

Clone the repository

git clone https://github.com/Ashish-1108/DermacScribe_AI
cd DermacScribe_AI


Create a virtual environment

On Windows:

python -m venv venv
.\venv\Scripts\activate


On macOS/Linux:

python3 -m venv venv
source venv/bin/activate


Install dependencies

pip install -r requirements.txt


(Optional) Build the database
If a script like build_database.py exists, run it to build/populate products.db (as indicated in README). 
GitHub

Set up API keys
Create a file ./.streamlit/secrets.toml and include keys like:

GEMINI_API_KEY = "YOUR_GEMINI_API_KEY_HERE"
OPENWEATHER_API_KEY = "YOUR_OPENWEATHERMAP_API_KEY_HERE"


Run a chosen feature

streamlit run 2_AI_Face_Check.py


Or run whichever .py file corresponds to the feature you want.

Usage Flow

Once running, a user can:

Choose a feature (via UI or menu)

For product analyzer: Enter or upload skincare product list → get compatibility/conflict report

For face scan: Upload image or input text concerns → get tailored product/routine advice

For genetic risk: Answer a quick questionnaire → get hereditary skin condition insights

For routine quiz: Answer questions about lifestyle/habits → receive ‘regi‐score’ and suggestions

For ingredient glossary: Search for an ingredient to learn its function, compatibility, caution

For UV notifier: Grant location access → receives daily UV index alert + sunscreen advice

Intended Audience & Use-Case

Consumers who want smarter, safer skincare routines rather than just trend-following.

Dermatology-adjacent apps/services looking to integrate ingredient analysis, AI-advice or UV alerts.

Skincare product developers/marketers who can embed ingredient compatibility logic.

Educational use for skincare professionals, health coaches or researchers exploring skin-tech/AI.

Limitations & Disclaimer

Not a substitute for professional medical advice: the tool is for informational and educational purposes only. Always consult a qualified dermatologist for any skin concerns. 
GitHub

Data / Model quality: The reliability depends on quality of ingredient database, AI model (Gemini or similar), face-scan accuracy, and user inputs.

Privacy & data security: As with any image upload or health-related tool, make sure to handle data securely and comply with relevant regulations.

Geolocation & weather/UV data: UV notifier requires accurate location and can vary by region/time; not all weather APIs are flawless.

Contributing

If you would like to contribute:

Pull requests are welcome: fix bugs, add new features (e.g., more skin concerns, new databases, model improvements)

Please ensure tests pass (if any exist in test/ folder)

Update documentation (README, docstrings) accordingly

Respect the licence (check repository for license)

Future Roadmap (Suggestions)

Add more skin conditions and deeper medical insights (with dermatologist collaboration)

Improve face‐scan model with advanced vision models (e.g., CNN/ViT for skin-lesion detection)

Expand ingredient database and compatibility rules (including allergen detection, personal sensitivities)

Mobile or web-based version (beyond Streamlit) for broader reach

User profile, history tracking and personalised recommendation engine

Offline mode or local model support to reduce dependency on external APIs

License

Please refer to the LICENSE file in the repository (if present) for terms of use.
(If no license is included, assume “All rights reserved” or contact the author.)

Quick Links

Repository: https://github.com/Ashish-1108/DermacScribe_AI

Author: Ashish-1108

Contact/Issues: Use GitHub issues on the repository
