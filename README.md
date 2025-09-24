# Predicting Mental Health Outcomes through Graph-Based Modelling

## 🧠 About This Project

This was my MSc Data Science dissertation research exploring a fundamental question: **Can we better understand mental health by modeling relationships rather than just symptoms?**

Traditional approaches often treat mental health factors in isolation. This project flips that perspective, using graph neural networks to represent how different aspects of mental health interconnect  because in reality, our wellbeing exists in a network of relationships, not a spreadsheet.

## 🔍 The Insight That Surprised Me

The most fascinating finding wasn't just that graph models worked well, but *which* one worked best. Despite theoretical advantages, the Graph Attention Network (GAT)  designed to identify "important" relationships actually underperformed. The winner was **GraphSAGE**, which achieved 96.8% accuracy by considering collective neighborhood patterns.

This suggests something profound about mental health: sometimes the broader context matters more than any single "key" factor. It's a reminder that in human-centric AI, the most elegant mathematical solution isn't always the most effective one.

## Motivation
Mental health disorders, such as depression, are complex and influenced by a network of factors. Traditional machine learning models often treat these factors in isolation, missing the relational context. This project investigates whether graph-based models can capture these intricate relationships to improve prediction and provide deeper insights.

## Methods
I implemented three state-of-the-art GNN architectures:
- **Graph Convolutional Network (GCN)**
- **Graph Attention Network (GAT)**
- **GraphSAGE**

The models were trained on a graph constructed from the [Social Media and Mental Health dataset](https://www.kaggle.com/datasets/souvikahmed071/social-media-and-mental-health) from Kaggle. The graph nodes represent individuals, and edges are based on feature similarity. The project followed the CRISP-DM methodology and used PyTorch Geometric for model implementation.


## 🛠️ What's Inside

- **Data Pipeline**: Processing and balancing mental health survey data with careful attention to ethical handling
- **Graph Construction**: Transforming tabular data into meaningful graph structures using cosine similarity
- **Three GNN Architectures**: Implementation of GCN, GAT, and GraphSAGE with PyTorch Geometric
- **Comprehensive Evaluation**: Accuracy metrics, confusion matrices, and embedding visualizations (t-SNE, PCA, UMAP)
- **Ethical Framework**: Considerations for responsible AI in mental health applications

  
## Key Results 📊
- Model	Accuracy	Precision	Recall	F1-Score
- GraphSAGE	96.8%	96.9%	96.8%	96.8%
- GAT	46.4%	55.2%	46.4%	42.7%
- GCN	46.0%	43.6%	46.0%	44.0%

- **GraphSAGE** significantly outperformed the other models, achieving **96.8% accuracy** in classifying depression severity.
- **GCN** and **GAT** showed lower performance (around 46% accuracy), highlighting the importance of the aggregation method in GNNs.
- The success of GraphSAGE suggests that inductive learning and neighborhood aggregation are particularly effective for this type of data.
- Also explore the the pythin file attached for a step-by-step walkthrough of the methodology.

## Installation and Usage
### Dependencies
The project requires Python 3.7+ and the following libraries:
- torch
- torch-geometric
- scikit-learn
- pandas
- numpy
- matplotlib
- seaborn
- imblearn

### Running the Code
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mental-health-gnn.git
   cd mental-health-gnn

- 📚 Citation
If this work inspires your research, please cite
Okorie, I. K. (2025). Predicting Mental Health Outcomes through Graph-Based Modelling. MSc Dissertation, University of Salford. *uploading link soon*
