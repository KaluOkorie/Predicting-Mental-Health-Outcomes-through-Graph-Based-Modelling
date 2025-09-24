# Predicting Mental Health Outcomes through Graph-Based Modelling

## Overview
This repository contains documentation for my MSc Data Science dissertation project at the University of Salford. The project explores the application of Graph Neural Networks (GNNs) to predict mental health outcomes, specifically depression severity, by modelling individuals and their attributes as a graph.

## Motivation
Mental health disorders, such as depression, are complex and influenced by a network of factors. Traditional machine learning models often treat these factors in isolation, missing the relational context. This project investigates whether graph-based models can capture these intricate relationships to improve prediction and provide deeper insights.

## Methods
I implemented three state-of-the-art GNN architectures:
- **Graph Convolutional Network (GCN)**
- **Graph Attention Network (GAT)**
- **GraphSAGE**

The models were trained on a graph constructed from the [Social Media and Mental Health dataset](https://www.kaggle.com/datasets/souvikahmed071/social-media-and-mental-health) from Kaggle. The graph nodes represent individuals, and edges are based on feature similarity. The project followed the CRISP-DM methodology and used PyTorch Geometric for model implementation.

## Key Results
- **GraphSAGE** significantly outperformed the other models, achieving **96.8% accuracy** in classifying depression severity.
- **GCN** and **GAT** showed lower performance (around 46% accuracy), highlighting the importance of the aggregation method in GNNs.
- The success of GraphSAGE suggests that inductive learning and neighborhood aggregation are particularly effective for this type of data.

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
