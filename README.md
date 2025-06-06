# ASReview Simulation: Evaluation of Machine Learning Strategies for Literature Screening

This repository contains the data, configurations, and raw outputs of a simulation study conducted using [ASReview Makita](https://asreview.ai/) to evaluate multiple machine learning classifiers and feature extraction strategies in the context of systematic literature reviews.

## Project Structure

├── data/ # Input datasets used for the simulation
├── config/ # Configuration files for Makita 
├── resultados/ # Raw outputs of the simulation runs
├── README.md # 
├── LICENSE # 
└── .gitignore # 


## How to Reproduce

We used `asreview-makita` with the following command (paths adjusted for reproducibility):

```bash
asreview makita template multimodel \
  -s ./data \
  --job_file config/makx1.sh \
  -o ./resuls \
  --classifiers svm rf logistic nb \
  --feature_extractors tfidf doc2vec \
  --impossible_models nb,doc2vec \
  --no_wordclouds \
  --n_runs 100 \
  --init_seed 155 \
  --model_seed 100

Install Makita with:
pip install asreview-makita

## License

- Code and configuration files are shared under the **MIT License**.
- Datasets and raw outputs are shared under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** .

About the Data
The data/ folder includes two anonymized datasets used for simulation:
	•	CTA_data.csv: Title and Abstract Screening dataset
	•	CTC_data.csv: Full-text Screening dataset
Each CSV includes a title, abstract, DOI and a binary relevance label.



