# Virtual Foundation Shade Matcher
Try on the right foundation before you buy it.

A web application that uses real-time computer vision to analyze your skin tone from a photo and recommend the perfect foundation shade from top cosmetic brands  instantly, virtually, and accurately.


### What It Does?

Most people waste money buying the wrong foundation shade. This app solves that.

Upload a photo, select a skin region (cheek, forehead, etc.), and the app extracts the average RGB values from that area to classify your skin tone. It then recommends foundation shades matched precisely to your complexion.


### Key Features
Upload image and select facial region

Extract RGB values from the selected area

Classify skin tone (Fair, Light, Medium, Olive, Dark, Deep Dark)

Recommend foundation shades from multiple brands

Display product images with suggestions

Dynamic interaction between frontend and backend



### Tech Stack
Backend -> Python 3.12, Flask, Flask-CORS

Frontend ->  JavaScript, HTML, CSS

Image Processing -> Custom RGB extraction & flood-fill algorithm

Skin Analysis ->  Rule-based RGB classifier 


### Project Structure

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
       


### Getting Started

#### Prerequisites
Python 3.12+

pip

#### Installation

terminal:clone the repository

cd VirtualFoundationShadeMatcher/ShadeMatch

-> Create and activate virtual environment

python -m venv venv

venv\Scripts\activate      # Windows

source venv/bin/activate   # macOS/Linux

-> Install dependencies

pip install flask flask-cors

-> Run the app

python app.py

Then click link in your browser.


### API Reference
POST /upload-rgb

Accepts pixel RGB data from the frontend canvas, computes average skin color, classifies the skin tone, and returns matched foundation shades.

### Roadmap
 Machine learning–based skin tone classification.
 
 Live webcam support for real-time shade detection.
 
 Expanded brand database with price filtering.
 
 AR overlay to virtually try on shades.
 
 Mobile-responsive redesign.


 ### Built with love to make beauty more inclusive and accessible for every skin tone.
