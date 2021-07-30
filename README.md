## Quickstart

```
# Clone this repo
git clone https://github.com/valerielimyh/multi_features_multiclass_text_classification.git

# Install the required dependencies and view the notebooks
cd multi_features_multiclass_text_classification
poetry install
poetry run jupyter lab
```

Repo to create containerized ML web service of this project can be found [here](https://github.com/valerielimyh/fastapi_ml_pytest)


- Dataset is derived from:

T. Bertin-Mahieux, D. P.W. Ellis, B. Whitman, and P. Lamere. The million song dataset. In
Proceedings of the 12th International Conference on Music Information Retrieval (ISMIR),
2011.
A. Schindler and A. Rauber. Capturing the temporal domain in Echonest Features for improved
classification effectiveness. In Proceedings of the 10th InternationalWorkshop on Adaptive Multimedia Retrieval (AMR), 2012.


#### Features
* trackID: unique identifier for each song (Maps features to their labels)
* title: title of the song. Type: text.
* tags: A comma-separated list of tags representing the words that appeared in the lyrics of the song and are assigned by human annotators. Type: text / categorical.
* loudness: overall loudness in dB. Type: float / continuous.
* tempo: estimated tempo in beats per minute (BPM). Type: float / continuous.
* time_signature: estimated number of beats per bar. Type: integer.
* key: key the track is in. Type: integer/ nominal. 
* mode: major or minor. Type: integer / binary.
* duration: duration of the song in seconds. Type: float / continuous.
* vect_1 ... vect_148: 148 columns containing pre-computed audio features of each song. 
	- These features were pre-extracted (NO TEMPORAL MEANING) from the 30 or 60 second snippets, and capture timbre, chroma, and mfcc aspects of the audio. \
	- Each feature takes a continuous value. Type: float / continuous.
 

#### Labels

* trackID: unique id for each song (Maps features to their labels)
* genre: the genre label
	1. Soul and Reggae
	2. Pop
	3. Punk
	4. Jazz and Blues
	5. Dance and Electronica
	6. Folk
	7. Classic Pop and Rock
	8. Metal