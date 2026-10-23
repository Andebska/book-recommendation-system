# Book Recommendation System

An exploratory project comparing three approaches to recommending
books using book metadata and user ratings.

## Approaches

1. **Popularity-Based Ranking** - ranks books using a weighted rating.
2. **Content-Based Filtering** - uses TF-IDF representations of authors
   and original titles.
3. **Collaborative Filtering** - uses a sparse book-user rating matrix,
   TruncatedSVD, and nearest-neighbor search.

## Technologies

- Python
- pandas and NumPy
- scikit-learn
- SciPy sparse matrices
- Matplotlib and Seaborn
- Jupyter Notebook

## Dataset

This project uses the Goodbooks-10k dataset.

Source: https://github.com/zygmuntz/goodbooks-10k

The local data files are not included in this repository. Download the
required `books.csv` and `ratings.csv` files from the dataset source,
and place them in the same directory as the notebook.

The notebook currently uses a copy containing approximately 981,756
rating rows. This may differ from the six-million-rating version
described in the main dataset repository. Results can vary across
dataset versions.

The Goodbooks-10k repository identifies its dataset under the
Creative Commons Attribution-ShareAlike 4.0 International License.
Please retain the required attribution and review the applicable terms
when using or redistributing the data.

## How to Run

1. Clone or download this repository.
2. Create and activate a Python virtual environment.
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
4. Place `books.csv` and `ratings.csv` in the same directory as the notebook.
5. Start Jupyter Notebook:
    ```bash
    jupyter notebook book-recommendation-system.ipynb
    ```
6. Run the notebook cells from top to bottom.

## Limitations

- The content-based model uses only authors and original titles.
- Recommendation examples are inspected qualitatively; formal offline evaluation has not been implemented.
- Results depend on the version and coverage of the dataset.
- The collaborative model requires rating data for the queried book.
