
# Spotify Music Recommendation System

This project presents a Music Recommendation System built using the Spotify dataset. The system leverages advanced data analysis and machine learning techniques to recommend songs based on user preferences.

## Features

- **Data Extraction**: Uses Spotipy to fetch song data from the Spotify Web API.
- **Exploratory Data Analysis (EDA)**: Identifies key features and patterns in the Spotify dataset.
- **Feature Engineering**: Selects relevant features to build an accurate recommendation model.
- **Recommendation System**: Recommends songs based on user-input songs using cosine similarity.

## Installation

1. **Clone the repository**:
  
2. **Install the required libraries**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up Spotify API credentials**:
   - Create an app on the [Spotify Developer's page](https://developer.spotify.com/).
   - Save your Client ID and Secret Key.
   - Set the environment variables:
     ```bash
     export SPOTIFY_CLIENT_ID='your_client_id'
     export SPOTIFY_CLIENT_SECRET='your_client_secret'
     ```

## Usage

1. **Import necessary libraries**:
   ```python
   import spotipy
   from spotipy.oauth2 import SpotifyClientCredentials
   import pandas as pd
   import numpy as np
   from collections import defaultdict
   from sklearn.metrics import euclidean_distances
   from scipy.spatial.distance import cdist
   import difflib
   import os
   ```

2. **Authenticate and initialize Spotipy**:
   ```python
   sp = spotipy.Spotify(auth_manager=SpotifyClientCredentials(client_id=os.environ["SPOTIFY_CLIENT_ID"],
                                                              client_secret=os.environ["SPOTIFY_CLIENT_SECRET"]))
   ```

3. **Define functions to fetch song data and calculate recommendations** (full code provided in the repository).

4. **Get song recommendations**:
   ```python
   recommended_songs = recommend_songs([
       {'name': 'Come As You Are', 'year': 1991},
       {'name': 'Smells Like Teen Spirit', 'year': 1991},
       {'name': 'Lithium', 'year': 1992},
       {'name': 'All Apologies', 'year': 1993},


-