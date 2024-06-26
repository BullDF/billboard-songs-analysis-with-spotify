# Billboard Hot Songs Analysis with Spotify

-- by Johnny Meng

Welcome to my project on analyzing songs with the Spotify API 🎵. This project borrowed [this dataset on the hot 100 songs on Billboard](https://www.kaggle.com/datasets/dhruvildave/billboard-the-hot-100-songs) from Kaggle as an entry point. From here, I randomly sampled 5000 songs and used the Spotify API to extract these songs from Spotify along with their audio features and popularity. Click to read more about the [Spotify web API](https://developer.spotify.com/documentation/web-api).

To use the Spotify API, I wrote a program importing the [Spotipy Python library](https://spotipy.readthedocs.io/en/2.22.1/?highlight=start#). The Python program can be found in the [`spot.py`](https://github.com/BullDF/billboard-songs-analysis-with-spotify/blob/main/data/spot.py) file in the GitHub repository. **To use this file, a file named `config.py` needs to be created locally that contains a `CLIENT_ID` and a `CLIENT_SECRET`, which can be obtained from the [Spotify web API](https://developer.spotify.com/documentation/web-api) website.**

The data exploration report can be found [here](https://github.com/BullDF/billboard-songs-analysis-with-spotify/blob/main/EDA/report.pdf).

For some machine learning analysis, I wrote another program to pull information on artist genres from Spotify again. I selected 7 famous music genres. If the music genre for an artist is not on the list, then the artist was marked as *other*. For analysis, I merged the information into a single dataset with all the audio features and the genres of the tracks and split the dataset into a training set and a test set using an 80:20 ratio. The program pulling this information from Spotify can be found in the [`genre.py`](https://github.com/BullDF/billboard-songs-analysis-with-spotify/blob/main/data/genre.py) file in the repo. The machine learning exploration report can be found [here](https://github.com/BullDF/billboard-songs-analysis-with-spotify/blob/main/ml_analysis/report/report.pdf).

An overview of the project with interactive EDA plots is included in [this project website](https://bulldf.github.io/billboard-songs-analysis-with-spotify/). Check it out at your leisure!