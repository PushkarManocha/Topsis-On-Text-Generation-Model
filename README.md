TOPSIS-Based Evaluation of Text Generation Models
#Overview

This project applies the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) multi-criteria decision-making method to evaluate and rank pre-trained text generation models based on multiple performance metrics. The approach enables an objective and transparent comparison of models by considering both qualitative and quantitative criteria.

#Key Features

Implements the TOPSIS algorithm for model ranking

Compares text generation models using multiple evaluation metrics

Supports both benefit and cost criteria

Produces a normalized decision matrix for fair comparison

Exports final rankings and scores to a CSV file for easy analysis

#Models Evaluated

The following pre-trained / fine-tuned text generation models are evaluated:

GPT-3.5

T5-Large

BERT Fine-Tuned

#Evaluation Criteria

Each model is assessed using the following metrics:

Criterion	Description	Type
Perplexity	Measures model uncertainty	Cost ↓
BLEU Score	Measures text generation accuracy	Benefit ↑
ROUGE Score	Measures content overlap	Benefit ↑
Execution Time	Time taken for text generation	Cost ↓
Memory Usage	Memory consumed during execution	Cost ↓

#Dataset Description

The dataset contains performance values of each model across the above metrics.
All criteria are normalized before ranking to ensure scale independence and fairness.

#Installation

Ensure Python 3.7 or higher is installed.
Install the required dependencies using:

pip install numpy pandas

#How to Run

Clone the repository:

git clone https://github.com/your-username/TOPSIS-Text-Generation.git
cd TOPSIS-Text-Generation


Run the TOPSIS evaluation script:

python topsis_text_generation.py


The ranked results will be saved automatically to:

topsis_results.csv

#Output

The script generates a ranked list of models based on their TOPSIS scores.

Sample Output:
Model	TOPSIS Score	Rank
GPT-3.5	0.87	1
T5-Large	0.72	2
BERT Fine-Tuned	0.65	3

Higher TOPSIS scores indicate better overall performance.

#TOPSIS Methodology

The TOPSIS algorithm follows these steps:

Decision Matrix Construction

Normalization of criteria values

Weight Assignment based on importance

Identification of Ideal and Negative-Ideal Solutions

Distance Calculation from ideal points

Score Computation and Ranking

#Project Structure
TOPSIS-Text-Generation/
│
├── topsis_text_generation.py
├── dataset.csv
├── topsis_results.csv
└── README.md

#Author

Pushkar Manocha
Roll No: 102303751
Thapar Institute of Engineering and Technology