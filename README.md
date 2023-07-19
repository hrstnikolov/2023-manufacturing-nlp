# Manifacturing Processes NLP

## Summary

Objective 


##  Procedude

### Steps, generalized
1. Get data.
1. Make embeddings.
1. Simple semantic search.
1. Dimensionality reduction.
1. Visualize the embeddings.
1. Annotation (label assignment) three ways:
   - topic modeling
   - manual
   - few-shot learining
1. Deploy.


### Steps, detailed
1. Scrape summaries of wikipedia articles describing manifacturing processes (e.g. soldering, milling...).
1. Assign a vector to each summary so that similar processes have similar vectors.
   - 384-dimension vector using SentenceTransformers
   - ~10_000-dimension vector using TF-IDF
1. Create function that returns the most similar processes to a new unseen description that the user provides. Do for both vector representations and compare.
1. Convert the 384-dimension vector representation to 2D vector.
1. Create an interactive plot to visualize the 2D representations of the processes.
1. Annotating (добяване на етикети).
   - Automatically group the processes by topic.
   - Showcase manually annotating in Jupyter Lab.
   - Create automatic predictor of how complex a process is by providing small number of examples (e.g. 50).
1. Create web application as final product. It shall have the following features:
   - search a process by index -> the app shows top 10 closest processes (and its score, how close it is)
   - search process by asking free-text question -> app again show top 10 closest
   - ask a question "how much X" -> get quantity

TODO ### How / tool used / implementation
1. Scraped from Wikipedia.
1. `SentenceTransformers`, use the `all-MiniLM-L6-v2` model. `TfidfVectorizer` from `sklearn.feature_extraction.text`.
1. Using cosine similarity function.
1. From the `umap` module use the `UMAP` class. Another option: `TruncatedSVD`.
1. Use `Bulk` although other several libraries are available ( `altair`, `bokeh`, `plotly`).
- Data needs to be in a specific format in csv.
- Позволява да запазим част от данните, който са ни интересни в .csv.
1. Annotation
   - `BERTopic`
   - `Pigeon`
   - `SetFit`
1. `Streamlit`


