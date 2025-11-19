# Overview

In the file dataset/training_data.csv you will find dataset containing news headlines and their tags: 0, if the headline is fake news, and, 1, if the headline is real news.

Your goal is to build a classifier that is able to distinguish between the two.

Once you have a classifier built, then use it to predict the labels for dataset/testing_data.csv. Generate a new file where the label 2 has been replaced by 0 (fake) or 1 (real) according to your model. Please respect the original file format, do not include extra columns, and respect the column separator.

## Dataset

The dataset are headlines of real news and fake news we have to predict.

This project uses [GloVe 300d](http://nlp.stanford.edu/data/glove.6B.zip).

## Project Description

The dataset given was pretty clean, mosrtly balanced labels and with no further problems more than a single BOM value. No clean needed after this also as featuring.

Our project has tested different models:

- [Random Forest Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
- [Logistic Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
- [Multinominal NB](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html)
- [XGBoost Classifier](https://xgboost.readthedocs.io/en/stable/)

Getting better results using *Logistic Regression* with a 94% accuracy and a 95%, wich is good. 

# Key Learning Points

## Cleaning and Lemmatizing
Since our dataset was very clean from the beginning, we don't need to check much things than the balancing wich os not needed for our dataset (balance of 51% vs 49%), so we just clean by striping and removing tabulators as "\t" and some other little things our dataset may have. Also we lemmatize our text.

## Vectorizing
While trining models with text, they expect actually numbers or numeric data; vectorizded data indeed should be fine to work, so in order to fir our models, vectorizing is an important thing to do. We learned how to vectorize using different methods suchs as BoW or TD-IFD, and using embeddings as well such as GloVe.

# Results
The final LogisticRegression model achieved:

| Metric         | Class | Precision | Recall | F1-Score | Support |
|----------------|-------|-----------|--------|----------|---------|
| Accuracy       |       |           |        |          | 0.9419  |
| Fake           | Fake  | 0.95      | 0.94   | 0.94     | 3515    |
| Real           | Real  | 0.93      | 0.95   | 0.94     | 3316    |
| Macro Avg      |       | 0.94      | 0.94   | 0.94     | 6831    |
| Weighted Avg   |       | 0.94      | 0.94   | 0.94     | 6831    |

# Future Improvements

**Import pre-models:** Models such as Bert or GPT-2 can be imported to use directly or fine tune to our problem.

**Test different embeddings:** Since lacking of time and havin other issues related to dependences for tensorflow, we cannot test much more embeddings such as FastText or many others.

## Project Structure
```bash
Project03_IronKaggle/
├── data/ # folder for csv and predictions files
│   ├── (files.csv) # many csv files
├── main.ipynb # main project
├── presentation.pdf # presentation in PDF format
├── README.md # current readme <:
```

## Installation
```bash
# Clone repository
git clone https://github.com/iKebb/Project05_NLP.git
```

## Contributors

<table align="center">
  <tr>
    <td align="center">
      <a href="https://github.com/iKebb">
        <img src="https://avatars.githubusercontent.com/u/82987736?v=4" width="100px;" alt="Keberth"/><br>
        <sub><b>Keberth</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/diogosimoez">
        <img src="https://avatars.githubusercontent.com/u/78166694?v=4" width="100px;" alt="Diogo"/><br>
        <sub><b>Diogo</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/JaviGARES">
        <img src="https://avatars.githubusercontent.com/u/230015620?v=4" width="100px;" alt="Javier"/><br>
        <sub><b>Javier</b></sub>
      </a>
    </td>
  </tr>
</table>

## License

This project is free of license. Feel free to use it!

## Contact

- **Via E-mail** - [keberth12@gmail.com](mailto:keberth12@gmail.com)
- **Via LinkedIn** - [Keberth José Rodríguez Albino](https://www.linkedin.com/in/keberth-josera-vkse1666)

Repo link: https://github.com/iKebb/Project05_NLP/