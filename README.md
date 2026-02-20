# Assignment 4: Customer Segmentation with Clustering

## Overview

This project implements a customer segmentation analysis for a UK-based online gift retailer using K-means clustering. The analysis segments customers based on their transaction history (2009-2011) using RFM (Recency, Frequency, Monetary) features to identify distinct customer groups and provide targeted marketing recommendations.

### Key Objectives
- Aggregate transaction data to customer-level RFM features
- Determine optimal number of clusters using elbow method and silhouette analysis
- Train K-means clustering model to segment customers
- Visualize and interpret customer segments
- Provide actionable business recommendations for each segment

## Project Structure

```
Assignment-4/
├── README.md                    # Project documentation (this file)
├── starter_notebook.ipynb       # Main Jupyter notebook with analysis
└── data/
    └── online_retail_II.csv     # Transaction dataset (2009-2011)
```

## Data Description

The `online_retail_II.csv` dataset contains transaction records with the following key fields:
- **Invoice**: Unique transaction identifier
- **StockCode**: Product code
- **Description**: Product name
- **Quantity**: Number of items purchased
- **InvoiceDate**: Transaction date and time
- **Price**: Unit price per item
- **Customer ID**: Unique customer identifier
- **Country**: Customer's country

## How to Run

### Option 1: Using Jupyter Notebook in VS Code

1. **Open the notebook:**
   - Open `starter_notebook.ipynb` in VS Code

2. **Install dependencies:**
   - Run the first code cell to install required packages:
     ```bash
     pip install pandas matplotlib seaborn scikit-learn
     ```

3. **Run the analysis:**
   - Execute cells sequentially from top to bottom
   - Fill in the TODO sections as you progress through the assignment

### Option 2: Using Terminal

1. **Install dependencies:**
   ```bash
   pip install pandas matplotlib seaborn scikit-learn
   ```

2. **Launch Jupyter:**
   ```bash
   jupyter notebook starter_notebook.ipynb
   ```
   Or:
   ```bash
   jupyter lab
   ```

3. **Execute the notebook:**
   - Run cells in order, completing the TODO sections

## Notebook Structure

The analysis is organized into six main steps:

### Step 1: Import Libraries and Load Data
- Import required Python libraries
- Load the Online Retail II dataset
- Display basic dataset information

### Step 2: Aggregate Transaction Data to Customer-Level RFM Features
- Clean transaction data (remove missing IDs, returns, etc.)
- Calculate RFM metrics for each customer:
  - **Recency**: Days since last purchase
  - **Frequency**: Number of unique transactions
  - **Monetary**: Total amount spent

### Step 3: Standardize Features and Determine Optimal k
- Standardize RFM features using StandardScaler
- Apply elbow method to test k values from 2 to 10
- Calculate silhouette scores for cluster quality validation
- Select optimal k value with written justification

### Step 4: Train K-Means Model and Visualize Segments
- Train final K-means model with optimal k
- Add cluster labels to customer data
- Create scatter plot visualization (Frequency vs Monetary)
- Calculate and display cluster centers

### Step 5: Interpret Segments and Provide Business Recommendations
- Analyze each customer segment's characteristics
- Provide descriptive names for segments
- Calculate detailed statistics for each segment

### Step 6: Submit Your Work
- Verify all code runs without errors
- Push to GitHub
- Submit repository link

## Submission

After completing all steps:

```bash
git add .
git commit -m 'completed customer segmentation assignment'
git push
```

Submit your GitHub repository link on the course platform.