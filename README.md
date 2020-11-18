# Recsys-arXiv
Using collaborative fitting, recommend similar authors to a user.

### Main Dataset
arxiv-metadata-oai-snapshot.json from https://www.kaggle.com/Cornell-University/arxiv

### DBLP V10 for Citaiton Graph
wget https://lfs.aminer.cn/lab-datasets/citation/dblp.v10.zip

### Data Preprocessing

<ol>
  <li><a href="https://github.com/malvo06/Recsys-arXiv/blob/main/Data_Conversion.ipynb">Data Conversion:</a> Opens the json files and saves them into pkl. Also has converts DBLP into a Graph</li>
  <li><a href="https://github.com/malvo06/Recsys-arXiv/blob/main/Data%20Organization.ipynb">Data Organization:</a> Reorganizes the dataframes and standardizes the format of authors names. Creates a table with all the papers each author can writen related to the author. Creates another table to form a dictionary to build an author to author graph based on collaboration.</li>
</ol>

### Models
<h3><a href="Memory Based Collaborative Filtering.ipynb">Memory Based Collaborative Filtering </a></h3>
This notebook has the full model and can be used to find similar papers and users. The model is based on td-idf vectorization and cosine similarity. Then the results are analyzed for the most relavent authors.
