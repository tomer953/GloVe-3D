# GloVe-3D
Project to show GloVe output in a visual way

## Train Model

We used [GloVe](https://github.com/stanfordnlp/GloVe) with the following models:
1. Wikipedia
	- downloaded pre-trained model
2. Game of thrones books
	- we used "A song of ice and fire" books 1-5, and convert them into single corpus file which Glove can read
	- train the model for this custom corpus (using custom demo.py script)

## GloVe's output:
Now the output is vectors.txt, and vocab.txt
- vocab.txt - the Frequency distribution file for each word
- vectors.txt - the words as vectors

## Using the output to find distance
We can now run two python scripts included in the GloVe project, for finding:
1. distance
	- Usage: `python c:/glove/results/distance.py`
2. word-analogy
	- Usage: `python c:/glove/results/distance.py`

# Data Visualisation
To take the output to the next level, we decided to visualizes it, as a high-dimensional vector spaces

## Choose the UI
we used this [repository](https://github.com/anvaka/pm/tree/master/about#software-galaxies-documentation), which visualizes dependencies from popular package managers and **modified it to use our own data-sets.**

## Build graph data
for doing so we needed to convert the Glove output (vectors.txt), to a valid graph input.
so we used this [repository](https://github.com/anvaka/word2vec-graph) to build a valid output.

## Upload graph data to a server
we used node [express.js](https://expressjs.com/) library to run a local server.
then we uploaded the graph data to a `public` folder, later we will point our UI Web application to use this data.

# Running the UI
we modified the `config.js` file of the pm project, and pointed the data to our own server.
then after few modification, the ui is ready to use and run our own custom graphs.

