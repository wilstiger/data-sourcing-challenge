
# Geomagnetic Storm Prediction - NASA API Data Sourcing Challenge

This repository contains the completed solution for the Module 6 Challenge of the AI Bootcamp, which involves requesting and processing CME (Coronal Mass Ejections) and GST (Geomagnetic Storms) data from NASA's DONKI API. The data is cleaned, processed, merged, and finally exported as a CSV for use in predicting geomagnetic storms.

## Table of Contents

- [Background](#background)
- [Challenge Description](#challenge-description)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies](#technologies)

## Background

Geomagnetic storms (GSTs) are caused by Coronal Mass Ejections (CMEs), massive bursts of plasma emitted from the Sun. These interactions with Earth's magnetic shield can disrupt electronic systems, power grids, and satellite communications. The NOAA Space Weather Prediction Center aims to predict these geomagnetic storms using data sourced from NASA's DONKI API.

This project involves collecting CME and GST data, merging it, and computing the average time it takes for a CME to cause a GST.

## Challenge Description

The challenge is divided into three parts:

1. **Part 1: Request CME Data from NASA's DONKI API** - Extract CME data, clean and filter the results, and identify linked GST events.
2. **Part 2: Request GST Data from NASA's DONKI API** - Extract GST data, clean, and identify linked CME events.
3. **Part 3: Merge and Clean Data for Export** - Merge the CME and GST data, compute the time difference between events, and export the final dataset to CSV.

## How It Works

1. **CME Data**: 
   - Request CME data from the NASA API for the specified date range.
   - Filter and clean the data, focusing on linked GST events.

2. **GST Data**: 
   - Request GST data from the NASA API for the specified date range.
   - Filter and clean the data, focusing on linked CME events.

3. **Merge and Export**:
   - Merge the CME and GST datasets.
   - Compute the time difference between CME start time and GST occurrence.
   - Export the final merged dataset as a CSV.

## Installation

To run this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   ```

2. Navigate to the project directory:
   ```bash
   cd data-sourcing-challenge
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file to store your NASA API key securely:
   ```bash
   touch .env
   ```
   Add the following to the `.env` file:
   ```bash
   NASA_API_KEY=your_nasa_api_key
   ```

5. Run the Jupyter notebook `retrieve_data.ipynb` to collect and process the data.

## Usage

1. After completing the installation, run the Jupyter notebook or Python script to request, process, and export the CME and GST data.
2. The final CSV file `merged_data.csv` contains the merged and cleaned dataset for further analysis.

## Technologies

- **Python**: Primary language for data processing.
- **Pandas**: For data manipulation and cleaning.
- **Requests**: To send API requests to NASA's DONKI API.
- **dotenv**: For loading environment variables, including API keys.
- **Jupyter Notebook**: For development and running the challenge code.
