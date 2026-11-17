# Additional Resources

_Links were compiled from well-known official sources; open each one before citing it in your portfolio, as sites occasionally move pages._

## Dataset and licence

- **[Google Play Store Apps (Kaggle, lava18)](https://www.kaggle.com/datasets/lava18/google-play-store-apps)** - The source dataset: both CSV files used in this project.
- **[Creative Commons Attribution 3.0](http://creativecommons.org/licenses/by/3.0/)** - Licence terms; attribution is required when sharing derived work.

## Python libraries (official documentation)

- **[pandas user guide](https://pandas.pydata.org/docs/user_guide/index.html)** - groupby, cut, crosstab, datetime handling, string methods.
- **[NumPy documentation](https://numpy.org/doc/stable/)** - Numerical arrays, log transforms.
- **[Matplotlib](https://matplotlib.org/stable/)** - Figure and axes API, saving figures.
- **[Seaborn](https://seaborn.pydata.org/)** - Histograms, boxplots, heatmaps, regplots.
- **[SciPy stats](https://docs.scipy.org/doc/scipy/reference/stats.html)** - spearmanr, kruskal, mannwhitneyu, chi2_contingency.
- **[scikit-learn: text feature extraction](https://scikit-learn.org/stable/modules/feature_extraction.html#text-feature-extraction)** - CountVectorizer used for the review word analysis.
- **[Jupyter / nbconvert](https://nbconvert.readthedocs.io/)** - Executing and exporting notebooks to HTML.
- **[python-docx](https://python-docx.readthedocs.io/)** - Used to generate the Word deliverables.

## Exploratory data analysis and statistics

- **Exploratory Data Analysis (John W. Tukey, 1977)** - The classic text that defined EDA.
- **[Python for Data Analysis, 3rd ed. (Wes McKinney)](https://wesmckinney.com/book/)** - Free online edition; pandas fundamentals from its creator.
- **[Python Data Science Handbook (Jake VanderPlas)](https://jakevdp.github.io/PythonDataScienceHandbook/)** - Free online; NumPy, pandas, Matplotlib and scikit-learn.
- **[Kaggle Learn](https://www.kaggle.com/learn)** - Short free courses: Pandas, Data Visualization, Data Cleaning.
- **[Bayesian average (weighted rating)](https://en.wikipedia.org/wiki/Bayesian_average)** - The idea behind the weighted rating in question A1.

## Text and sentiment analysis

- **[VADER sentiment (Hutto and Gilbert, 2014)](https://github.com/cjhutto/vaderSentiment)** - Rule-based sentiment model widely used for short reviews.
- **[NLTK](https://www.nltk.org/)** - Tokenisation, stop-words, sentiment tools.
- **[TextBlob](https://textblob.readthedocs.io/)** - Simple polarity and subjectivity scores.
- **[BERTopic](https://maartengr.github.io/BERTopic/)** - Next step: discover review themes bottom-up instead of with a keyword lexicon.

## Android and Play Store domain knowledge

- **[Google Play Console Help](https://support.google.com/googleplay/android-developer)** - Ratings, reviews, content ratings and store listing rules.
- **[Android vitals](https://developer.android.com/topic/performance/vitals)** - Crash and ANR metrics, relevant to the bug and crash findings.
- **[Android App Bundles](https://developer.android.com/guide/app-bundle)** - Modular delivery to reduce install size.

## Communicating results and portfolio building

- **Storytelling with Data (Cole Nussbaumer Knaflic)** - Designing charts that drive decisions.
- **[The Python Graph Gallery](https://python-graph-gallery.com/)** - Chart recipes in Matplotlib and Seaborn.
- **[GitHub Docs: About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)** - How to present a repository.
- **[Jupytext](https://jupytext.readthedocs.io/)** - Keep notebooks as clean, diff-friendly scripts (this project uses the same percent format).

## Ideas to extend this project

- Predict star-app probability with logistic regression or gradient boosting and report feature importance.
- Re-score reviews with a transformer model and compare to the provided sentiment.
- Topic-model the reviews (LDA or BERTopic) and compare with the keyword themes.
- Build an interactive dashboard (Streamlit, Power BI or Tableau) for the headline metrics.
- Collect repeated snapshots to compute true update intervals and seasonality (questions M6 and A2).
- Run a price-elasticity or category-saturation analysis for a go-to-market recommendation.
