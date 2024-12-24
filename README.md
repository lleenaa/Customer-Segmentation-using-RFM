# Customer Segmentation Using RFM  

## Overview  
This project focuses on **customer segmentation** using Recency, Frequency, and Monetary (RFM) analysis combined with clustering and association rule mining. The goal is to analyze customer behaviors, identify patterns, and help businesses create targeted marketing strategies to enhance sales and customer engagement.  

### Key Objectives  
1. Segment customers into meaningful groups based on their purchasing behavior.  
2. Extract frequent patterns and actionable association rules for each segment.  
3. Provide insights to improve marketing strategies and product recommendations.  

## Data Description  
The dataset contains **541,909 transactions** from UK retailers, covering:  
- **InvoiceNo**: Transaction identifier.  
- **StockCode**: Product identifier.  
- **Description**: Product description.  
- **Quantity**: Number of products purchased.  
- **InvoiceDate**: Date and time of the transaction.  
- **UnitPrice**: Price per unit.  
- **CustomerID**: Unique customer identifier.  
- **Country**: Country of the customer.  

### Preprocessing Steps  
1. **Data Cleaning**:  
   - Removed duplicates, missing values, and anomalies.  
   - Handled canceled transactions and negative quantities.  
2. **Feature Engineering**:  
   - Computed RFM values and additional features like average transaction value and favorite shopping day/hour.  
   - Added geographic and seasonal features for deeper insights.  
3. **Outlier Detection**:  
   - Used Isolation Forest to detect and remove outliers.  
4. **Dimensionality Reduction**:  
   - Applied PCA to retain 85% of the variance with six principal components.  

## Methodology  
### Clustering Techniques  
1. **K-Means**:  
   - Best performer with a silhouette score of **0.218**.  
2. **K-Medoids**:  
   - Weak separation of clusters with a silhouette score of **0.08**.  
3. **Hierarchical Clustering**:  
   - Silhouette score of **0.211**, but less effective than K-Means.  

### Cluster Profiles  
- **Cluster 0 - Local Shoppers**:  
  - Located mostly in the UK.  
  - Preference for tote bags and teacups with diverse patterns.  
- **Cluster 1 - Regular Shoppers**:  
  - Moderate purchasing behavior.  
  - Interest in party and cake-related items.  
- **Cluster 2 - Frequent Buyers**:  
  - High-frequency, high-monetary customers.  
  - Tend to buy practical and decorative items like tote bags and heart-shaped products.  

### Frequent Pattern Mining  
- Extracted frequent itemsets and association rules to identify shopping patterns.  
- Example: Customers buying "JUMBO BAG RED RETROSPOT" are likely to purchase other tote bags, enabling cross-selling opportunities.  

## Insights  
1. Enhance inventory management by stocking frequently bought product pairs.  
2. Develop cluster-specific marketing campaigns, such as bundle offers for Local Shoppers or premium decorative products for Frequent Buyers.  
3. Tailor recommendations based on association rules to boost cross-selling.  
