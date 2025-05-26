# Crime Prediction Using Neural Networks 👮♂️🔍

![Crime Prediction Banner](https://via.placeholder.com/800x200?text=Crime+Prediction+Using+Neural+Networks)

## Table of Contents
1. [Introduction](#introduction-)
2. [Dataset](#dataset-)
3. [Methodology](#methodology-)
4. [Models](#models-)
5. [Results](#results-)
6. [How to Run](#how-to-run-)
7. [References](#references-)

## Introduction 🚀
Welcome to the **Crime-Prediction** project! This repository replicates and extends the research from the paper ["Predicting Crime and Other Uses of Neural Networks in Police Decision Making"](https://www.frontiersin.org/articles/10.3389/fpsyg.2021.587943/full) by Steven Walczak. 

Using neural networks, we predict:
- 🕵️ Crime types
- 📍 Crime locations

based on historical crime data from **Detroit (2016-2020)**. Explore this README to learn about:
- Project's purpose
- Methodology
- Model architectures
- Performance results
- How to get started

## Dataset 📊
We use the **RMS Crime Incidents** dataset from the City of Detroit, containing:

| Feature | Description |
|---------|-------------|
| 📅 Date/Time | Incident timestamp |
| 🏙️ Location | Zip code |
| ⚖️ Crime Type | Offense category |

**Dataset Statistics:**
- Time period: 2016-2020
- Crime categories: 27 (filtered >600 incidents each)
- Zip codes: 30

📥 **Download:** [ResearchGate Dataset Link](https://www.researchgate.net/publication/123456789)

## Methodology 🧠
Our approach builds on the paper's methodology with enhancements:

### Data Preprocessing
1. Extracted key columns:
   - incident_day_of_week
   - incident_hour_of_day  
   - zip_code
   - offense_category

2. Filtered crime categories (600+ incidents)
3. Balanced training set
4. One-hot encoded categorical variables
5. Kept hour as numerical feature

### Crime Type Prediction Model
graph LR
    A[38 Input Features] --> B[12-node Hidden Layer]
    B --> C[4-node Hidden Layer]
    C --> D[27 Crime Categories]

### Location Prediction Model
graph LR
    A[35 Input Features] --> B[27-node Hidden Layer]
    B --> C[6-node Hidden Layer]
    C --> D[30 Zip Codes]

### Clone the Repository
git clone https://github.com/WasifSohail5/Crime-Prediction.git
cd Crime-Prediction

### Install Dependencies
pip install -r requirements.txt
