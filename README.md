# Deconstructing the Global Retail Customer Experience: A Transformer-Based Analysis of Thematic Drivers and Sentiment on Reddit

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)

**Author:** Mohammad Nikbakhtbideh  
**Affiliation:** Universiti Sains Malaysia (USM)  
**GitHub:** [inick-tech](https://github.com/inick-tech)

---

## 📝 Abstract
This repository contains the official code and analysis pipeline for the paper, "Deconstructing the Global Retail Customer Experience." This research investigates the primary drivers of customer satisfaction in the global retail sector by applying a state-of-the-art Natural Language Processing (NLP) pipeline to a large corpus of unsolicited customer feedback from Reddit. By integrating BERTopic for thematic discovery and a fine-tuned RoBERTa model for sentiment analysis, the study identifies three dominant thematic categories in customer discourse: **Physical**, **Cognitive**, and **Social**. Our findings indicate that while retailers meet expectations on price and value (Cognitive), significant customer friction exists in operational execution (Physical) and is most acutely felt in customer service interactions (Social).

## 📂 Repository Structure
The repository is organized to ensure clarity and reproducibility of the research findings.

```
Global-Retail-CX-Analysis/
│
├── 📂 data/
│   └── placeholder.txt         # Placeholder for the dataset (see Data section)
│
├── 📂 notebooks/
│   ├── 01_Main_Analysis.ipynb  # Jupyter notebook for data preprocessing, topic modeling, and sentiment analysis.
│   └── 02_Statistical_Analysis.ipynb # Jupyter notebook for statistical validation (Chi-Square, ANOVA).
│
├── 📂 results/
│   └── .gitkeep                # This directory will store generated charts and tables.
│
├── .gitignore                  # Specifies files to be ignored by Git.
├── LICENSE                     # MIT License for the project.
└── README.md                   # You are here.
```

## 🚀 Getting Started
To replicate the analysis, please follow the steps below.

### Prerequisites

* Python 3.9 or higher
* Jupyter Notebook or Google Colab
* Git for cloning the repository

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/inick-tech/Global-Retail-CX-Analysis.git](https://github.com/inick-tech/Global-Retail-CX-Analysis.git)
    cd Global-Retail-CX-Analysis
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate

    # For Windows
    python -m venv venv
    .\venv\Scripts\activate
    ```

3.  **Install the required libraries:**
    The necessary Python packages are listed in `requirements.txt`.
    ```bash
    pip install -r requirements.txt
    ```

### Data

Due to the terms of service of Reddit and to protect user privacy, the raw dataset (`reddit_retails_posts_2015_2025.csv`) used in this study is not included in this repository.

To run the notebooks, you will need to place your own dataset with a similar structure in the `/data` directory. The expected CSV file should contain at least the following columns:
* `title`: The title of the Reddit post.
* `body`: The main text content of the Reddit post.

## ⚙️ Usage: Running the Analysis

The analysis is divided into two main notebooks, which should be run sequentially.

1.  **`notebooks/01_Main_Analysis.ipynb`**:
    * This notebook handles the entire NLP pipeline:
        1.  Loads and preprocesses the raw text data.
        2.  Performs thematic discovery using **BERTopic** to identify latent topics.
        3.  Conducts sentiment analysis on each post using a fine-tuned **RoBERTa** model.
        4.  Maps the discovered topics to the theoretical framework (Physical, Cognitive, Social).
        5.  Generates the final visualizations and summary tables presented in the paper.

2.  **`notebooks/02_Statistical_Analysis.ipynb`**:
    * This notebook validates the findings from the main analysis using:
        1.  **Chi-Square Test:** To confirm the statistical significance of the relationship between thematic categories and sentiment polarity.
        2.  **One-Way ANOVA:** To assess whether the average sentiment scores vary significantly across the three themes.
        3.  **Descriptive Statistics:** To provide further insights into post length and sentiment scores per category.

## 📊 Key Findings

The analysis reveals a clear hierarchy of customer priorities and pain points in the global retail sector.

#### Thematic Distribution
[cite_start]Physical factors are the most frequently discussed, indicating that operational and logistical elements are top-of-mind for customers[cite: 7, 126].

![Frequency Distribution of Thematic Categories](./results/charts/Figure%201%20Frequency%20Distribution%20of%20Thematic%20Categories%20on%20Reddit.png)
[cite_start]*Figure 1: Frequency Distribution of Thematic Categories on Reddit.* [cite: 131]

#### Sentiment Polarity Across Themes
[cite_start]Social factors (customer service) are the primary source of customer friction, showing the highest proportion of negative sentiment[cite: 8]. [cite_start]In contrast, Cognitive factors (price & value) are associated with the most positive sentiment[cite: 9].

![Percentage Distribution of Sentiment within Each Thematic Category](./results/charts/Figure%202%20Percentage%20Distribution%20of%20Sentiment%20within%20Each%20Thematic%20Category.png)
[cite_start]*Figure 2: Percentage Distribution of Sentiment within Each Thematic Category.* [cite: 138]


## 📄 Citation
If you use the code or findings from this research in your work, please cite our paper:

```bibtex
@article{Nikbakhtbideh2025,
  title   = {Deconstructing the Global Retail Customer Experience: A Transformer-Based Analysis of Thematic Drivers and Sentiment on Reddit},
  author  = {Nikbakhtbideh, Mohammad},
  journal = {arXiv preprint},
  year    = {2025},
  url     = {[https://github.com/inick-tech/Global-Retail-CX-Analysis](https://github.com/inick-tech/Global-Retail-CX-Analysis)}
}
```

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
