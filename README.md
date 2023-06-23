# Manifacturing Processes NLP

## Summary

Objective 


##  Procedude

### Steps, verbose
1. Scrape summaries of wikipedia articles describing manifacturing processes (e.g. soldering, milling...).
1. Assign 384-dimension vector to each summary so that similar processes have similar vectors.
1. Convert the 384-dimension vector to 2D vector.
1. Create an interactive plot to visualize the 2D representations of the recipes.
1. Create function that returns the most similar recipes to an new recipe we provide. E.g. input recipe: Pork chops, closes recipes: Pork Cutlets, Breaded Pork Chops, Beef Chops.... Implement two ways:
   - SentenceTransformers + UMAP
   - TF-IDF


### Steps, generalized
1. Get data.
1. Make embeddings.
1. Dimensionality reduction.
1. Visualize interactively.
1. Simple semantic search.


TODO ### How / tool used / implementation
1. TODO
1. `SentenceTransformers`, use the `all-MiniLM-L6-v2` model.
1. From the `umap` module use the `UMAP` class. Another option: TruncatedSVD.
1. Use `Bulk` although other several libraries are available ( `altair`, `bokeh`, `plotly`).
- Data needs to be in a specific format in csv.
- Позволява да запазим група от подобни рецепти, който са ни интересни в .csv, т.е. да анотираме.
1. 


