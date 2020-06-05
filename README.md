## Learning song embeddings with Doc2Vec

The code in this repository was used to learn embeddings for songs using their lyrics.
Training data consists of 193 songs by the following artists:
- Blink-182
- Angels and Airwaves
- Box Car Racer

## Using the embeddings for playlist generation

The following steps were be taken to create [this spotify playlist](https://open.spotify.com/playlist/7E2MxIY1Heq1vz5BfyFrU9?si=1x-1HaV1QBCXgVCLQatKbA)

- A Doc2Vec PV-DM model was fit to the corpus of songs
- Song embeddings (high-dimensional vectors) were predicted for each song
- A similarity score was calculated between each pair of songs
- A spotify playlist was created by starting with one song, then finding to its next closet song that is not yet in the playlist
