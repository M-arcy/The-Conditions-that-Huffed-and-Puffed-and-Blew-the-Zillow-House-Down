

# The Conditions That Huffed and Puffed and Blew the Zillow House Down

## Table of Contents

- [Description](#description)
- [The Business Problem](#the-business-problem)
- [Key Findings](#key-findings)
- [Visuals](#visuals)
- [Installation](#installation)
- [Usage](#usage)
- [Presentation](#presentation)
- [Author](#author)

<hr style="border: none; height: 10px; background-color: #003057;" />

## Name

Predicting Housing Prices — Entity Academy Data Science Final Project

## Description

In February 2021, Zillow launched an AI-driven home-buying program, purchasing homes at scale to renovate and resell at a profit. Nine months later, it collapsed. The company lost an average of __$25,000 on every home it sold__, posted a $528 million loss, laid off 25% of its workforce, and was left holding 7,000 unwanted homes after its machine learning model failed to keep pace with a rapidly shifting market.

This project uses the same fundamental problem — predicting housing prices — to explore what a more grounded approach to that prediction might look like, and where Zillow's strategy went wrong.

Using the __Ames, Iowa housing dataset__ (1,460 homes sold 2006–2010, 79 feature variables) from Kaggle, the project moves through the full data science workflow: cleaning and encoding, exploratory analysis, feature correlation, and testing multiple predictive models across __Python__ and __R__, with visualizations built in __Tableau__ and __Excel__.

This project has these files:
- `Exploratory Analysis in Python/Visualization in Python.ipynb` — EDA, data cleaning, and correlation analysis in Python
- `Analysis in Python/Exploratory analysis housing data.ipynb` — feature engineering and data preparation
- `Analysis in Python/k-Means and K-Nearest Neighbors.ipynb` — KMeans clustering and KNN model
- `Data Analysis in R/House analysis in R.ipynb` — statistical modeling and stepwise regression in R
- `Visuals_Graphs/` — exported charts and figures used in the presentation
- `Train_and_test sets/` — prepared training and test datasets
- `Powerpoint in PDF/Final Project Presentation PDF.pdf` — slide deck from the February 2022 presentation
- `README.md` — provides an overview of the project

[Back to Top](#table-of-contents)

## The Business Problem

Zillow's iBuying algorithm failed in part because it treated housing price prediction as a pure modeling problem without enough grounding in what drives real-world housing value — condition, location context, and renovation potential. The goal of this project is to surface those drivers from the data and identify the kinds of properties where price prediction matters most.

**Central question:** What features most strongly predict sale price, and where do undervalued properties cluster in ways that suggest renovation opportunity?

[Back to Top](#table-of-contents)

## Key Findings

**Strongest predictor of sale price:**
Overall condition quality (`OverallQual`) had the highest correlation with `SalePrice` at __r = 0.79__ — the single most influential variable in the dataset.

**Renovation opportunity insight:**
One of the more revealing visualizations showed that homes with __lower overall condition scores are selling at disproportionately depressed prices__ relative to their other characteristics. These are the properties where targeted renovation would produce the largest price lift — precisely the strategy Zillow needed to execute, but didn't.

**Models tested:**
- K-Nearest Neighbors (Python)
- KMeans clustering (Python)
- Stepwise regression (R)
- Random Forest (Python)

**Data preparation:**
- 1,460 observations, 81 columns
- Dropped 20 non-predictive columns
- Imputed missing `LotFrontage` values with column mean (~70.05)
- Label-encoded categorical variables for model compatibility

[Back to Top](#table-of-contents)

## Visuals

Charts and figures generated during analysis are saved in the `Visuals_Graphs/` folder and include:
- Correlation heatmap showing relationships between all 79 features and `SalePrice`
- Condition score vs. price scatter plot revealing renovation opportunity clusters
- Bar graphs, histograms, and distribution plots from the EDA phase

The slide deck presentation (PDF) includes the full visual narrative presented to students, faculty, and prospective employers.

## Installation

Clone the repository:

```bash
git clone https://github.com/M-arcy/The-Conditions-that-Huffed-and-Puffed-and-Blew-the-Zillow-House-Down.git
cd The-Conditions-that-Huffed-and-Puffed-and-Blew-the-Zillow-House-Down
```

Create and activate a virtual environment (recommended):

```bash
python -m venv venv
# On Mac/Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

[Back to Top](#table-of-contents)

## Usage

Start with the exploratory analysis notebook to understand the data and key correlations:

```bash
jupyter notebook "Exploratory Analysis in Python/Visualization in Python.ipynb"
```

Then follow the modeling notebooks in order:

```bash
jupyter notebook "Analysis in Python/k-Means and K-Nearest Neighbors.ipynb"
```

The R analysis notebook (`Data Analysis in R/House analysis in R.ipynb`) covers stepwise regression and can be opened in JupyterLab with an R kernel installed.

The original Kaggle dataset is available at [kaggle.com/marcopale/housing](https://www.kaggle.com/marcopale/housing/).

[Back to Top](#table-of-contents)

## Presentation

This project was presented __February 21, 2022__ via Zoom to students, faculty, and prospective employers as the capstone for the Entity Academy / Woz U Data Science program.

- __[Watch the presentation on Vimeo](https://vimeo.com/680143023/)__ *(instructor critique begins at 35:17)*
- __[View the slide deck (PDF)](./Powerpoint%20in%20PDF/Final%20Project%20Presentation%20PDF.pdf)__

[Back to Top](#table-of-contents)

## Support

For questions, open an issue on the [GitHub repository](https://github.com/M-arcy/The-Conditions-that-Huffed-and-Puffed-and-Blew-the-Zillow-House-Down/issues) or reach out via [LinkedIn](https://www.linkedin.com/in/marcy-misner/).

## Author

Developed by __Marcy Misner__.

For more of my work: [GitHub](https://github.com/M-arcy) | [LinkedIn](https://www.linkedin.com/in/marcy-misner/)

## License

This project is licensed under the MIT License.

[Back to Top](#table-of-contents)
