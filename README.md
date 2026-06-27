# Virtual Foundation Shade Matcher
Try on the right foundation — before you buy it.
A web application that uses real-time computer vision to analyze your skin tone from a photo and recommend the perfect foundation shade from top cosmetic brands — instantly, virtually, and accurately.


# What It Does?

Most people waste money buying the wrong foundation shade. This app solves that.

Upload a photo, select a skin region (cheek, forehead, etc.), and the app extracts the average RGB values from that area to classify your skin tone. It then recommends foundation shades from brands like Fenty Beauty, MAC, NARS, Maybelline, Estée Lauder, and more — matched precisely to your complexion.


# Key Features
Pixel-level skin sampling — Uses an interactive canvas with flood-fill and masking to let users precisely select any skin region
RGB-based skin tone classification — Analyzes average pixel color to categorize skin into 6 tones: Fair, Light, Medium, Olive, Dark, and Deep Dark
Personalized foundation suggestions — Returns 3 matched shades per skin tone, each with brand name and product image
Interactive frontend — Upload, select, draw, and get results all in one smooth flow
REST API backend — Flask + Python backend with clean /upload-rgb endpoint, ready for integration or extension
Session-based result rendering — Results delivered via a dedicated results page with zero data leakage



# Tech Stack
LayerTechnologyBackendPython 3.12, Flask, Flask-CORSFrontendVanilla JavaScript, HTML5 Canvas APIImage ProcessingCustom RGB extraction & flood-fill algorithmSkin AnalysisRule-based RGB classifier (skincomplexity.py)Async APIFastAPI-compatible structure (FastAPI also installed)ServerGevent / Uvicorn ready


# Project Structure

VirtualFoundationShadeMatcher/
└── ShadeMatch/
    ├── app.py                  # Flask app & API routes
    ├── skincomplexity.py       # Skin tone classifier + foundation mapper
    ├── frontend/
    │   ├── Frontpage.html      # Landing page
    │   ├── UserInteraction.html # Upload & region selection UI
    │   ├── result.html         # Foundation recommendations page
    │   ├── main.js             # Canvas interaction logic
    │   ├── drawing.js          # Brush/mark drawing
    │   ├── floodFill.js        # Flood-fill region selection
    │   ├── extraction.js       # Pixel extraction from canvas
    │   ├── rgbData.js          # RGB data collection
    │   ├── contrast.js         # Contrast enhancement
    │   └── download.js         # Image download utility
    └── images/                 # Foundation shade reference images
        ├── ivory.jpg, porcelain.jpg, alabaster.jpg
        ├── beige.jpg, warmsand.jpg, lighthoney.jpg
        ├── naturalbeige.jpg, mediumgolden.jpg, mediumtan.jpg
        ├── oliviemedium.jpg, goldenolive.jpg, tan.jpg
        ├── deepbronze.jpg, cocoa.jpg, mocha.jpg
        └── espresso.jpg, ebony.jpg, richmaho.jpg


# Getting Started

# Prerequisites
Python 3.12+
pip

# Installation

bashgit clone https://github.com/yourusername/VirtualFoundationShadeMatcher.git
cd VirtualFoundationShadeMatcher/ShadeMatch

-> Create and activate virtual environment
python -m venv venv
venv\Scripts\activate      # Windows
source venv/bin/activate   # macOS/Linux

-> Install dependencies
pip install flask flask-cors

-> Run the app
python app.py
Then open http://localhost:5000 in your browser.


# API Reference
POST /upload-rgb
Accepts pixel RGB data from the frontend canvas, computes average skin color, classifies the skin tone, and returns matched foundation shades.


# Supported Skin Tones & Brands
Skin ToneRecommended BrandsFairMaybelline, L'Oreal, NARSLightMAC, Bobbi Brown, Estée LauderMediumFenty Beauty, BareMinerals, Too FacedOliveHuda Beauty, NARS, MACDarkFenty Beauty, Lancôme, RevlonDeep DarkBlack Opal, Estée Lauder, Iman


# Roadmap
 Machine learning–based skin tone classification (replace rule-based logic)
 Live webcam support for real-time shade detection
 Expanded brand database with price filtering
 AR overlay to virtually try on shades
 Mobile-responsive redesign

# Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

# License
This project is open source.

 # Built with love to make beauty more inclusive and accessible for every skin tone.
