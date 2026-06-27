# Virtual Foundation Shade Matcher
Try on the right foundation before you buy it.
A web application that uses real-time computer vision to analyze your skin tone from a photo and recommend the perfect foundation shade from top cosmetic brands  instantly, virtually, and accurately.


# What It Does?

Most people waste money buying the wrong foundation shade. This app solves that.

Upload a photo, select a skin region (cheek, forehead, etc.), and the app extracts the average RGB values from that area to classify your skin tone. It then recommends foundation shades matched precisely to your complexion.


# Key Features
Pixel-level skin sampling — Uses an interactive canvas with flood-fill and masking to let users precisely select any skin region.

RGB-based skin tone classification — Analyzes average pixel color to categorize skin into 6 tones: Fair, Light, Medium, Olive, Dark, and Deep Dark.

Personalized foundation suggestions — Returns 3 matched shades per skin tone, each with brand name and product image.

Interactive frontend — Upload, select, draw, and get results all in one smooth flow.

REST API backend — Flask + Python backend with clean /upload-rgb endpoint, ready for integration or extension.

Session-based result rendering — Results delivered via a dedicated results page with zero data leakage.



# Tech Stack
Backend -> Python 3.12, Flask, Flask-CORS
Frontend -> Vanilla JavaScript, HTML5 Canvas API
Image Processing -> Custom RGB extraction & flood-fill algorithm
Skin Analysis ->  Rule-based RGB classifier (skincomplexity.py)
Async API ->  FastAPI-compatible structure (FastAPI also installed)
Server -> Uvicorn ready


# Project Structure

VirtualFoundationShadeMatcher/
└── ShadeMatch/
    ├── app.py                  
    ├── skincomplexity.py       
    ├── frontend/
    │   ├── Frontpage.html      
    │   ├── UserInteraction.html
    │   ├── result.html         
    │   ├── main.js           
    │   ├── drawing.js          
    │   ├── floodFill.js        
    │   ├── extraction.js       
    │   ├── rgbData.js          
    │   ├── contrast.js         
    │   └── download.js        
    └── images           
       


# Getting Started

# Prerequisites
Python 3.12+
pip

# Installation

terminal: git clone https://github.com/yourusername/VirtualFoundationShadeMatcher.git

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

# Roadmap
 Machine learning–based skin tone classification.
 Live webcam support for real-time shade detection.
 Expanded brand database with price filtering.
 AR overlay to virtually try on shades.
 Mobile-responsive redesign.

# Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

# License
This project is open source.

 # Built with love to make beauty more inclusive and accessible for every skin tone.
