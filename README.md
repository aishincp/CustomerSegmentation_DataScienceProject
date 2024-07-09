# Customer Mall Segmentation Analysis

### 1. Purpose of the Project
The primary aim of this CUstomer Segmentation Analysis project is to gain deeper insights into the diverse customer base of the mall & develop targeted marketing strategies. Specifically, the project aims to:

1. <mark>Understand Customer Behavior</mark> (to identify patterns in shopping habits, spending techniques, and demographic characteristics)
  
2. <mark>Segment the Customer Base</mark> (meaningful segments based on key variables such as age, annual income & spending score)
  
3. <mark>Optimize Marketing Stratergies</mark> (use the gained insights from segmentation analysis to tailor marketing approaches, product offerings and customer experiences for each segment)


### 2. Analysis Approach
The analysis begins with an EDA to understand the characteristics of customer data.

#### 2.1 Univariate Analysis


a) _Age Distribution_
- The Age Distribution is right-skewed.
- Most customers are between 30-50 years old.

![Age Distribution](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/a6d3869c-6026-42ff-8b51-eb3d92cd23b7)

b) _Annual Income Distribution_
- The distribution is roughly normal.
- Most incomes fall between 40 (k$) and 80 (k$).

![Annual Income Distribution](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/fd14bd01-7eeb-4a9c-964d-12213a892b22)

c) _Spending Score Distribution_
- The distribution appears to be bimodal.
- This suggests two distinct groups of customers with different spending habits.

![Spending Score Distribution](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/615d6c13-8b49-4e53-be3b-bc953cde8635)

d) _Gender Distribution_
- There are more female customers (56%) than male customers (44%)

![Gender Distribution](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/4ee40b5e-70f8-4cd6-84c0-f229a6a2d95f)

#### 2.2 Bivariate Analysis
Now, let's examine the relation between pairs of variables:

a) _Age vs. Annual Income_
- No clear linear relationship is observed.
- Higher incomes are more common in the 30-60 age range.

b) _Annual Income vs. Spending Score_
- An interesting pattern is observed, suggesting potential customer segments.

c) _Age vs. Spending Score_
- Younger customers (below 40) seem to have a broader range of spending scores.

![Bivariate Analysis](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/8b38d4f2-430a-47f9-bb3f-69b9cb485d35)
  
#### 2.2 Multivariate Analysis
A correlation matrix is computed & visualized using a heatmap:

a) _Age and Spending Score_
- Moderate negative correlation (-0.327)
- As age increases, the spending score tends to decrease slightly.

b) _Annual Income and Spending Score_
- Very weak positive correlation (0.0099)
- Practically no linear relation between them.

c) _Age and Annual Income_
- Very weak negative correlation (-0.012)
- This suggests that age and income are not strongly related in this dataset.

![MultivariateAnalysis](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/06543c4d-1ad6-4749-a45f-6c5e6f017ecf)

![CorrelationMatrix](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/e7f65976-45eb-4e00-aa19-33a203bfb8e3)


### 2. K-Means Clustering (Bivariate Clustering)

The insights from the analysis are used to move on to K-Means clustering to identify distinct customer segments.
![Clustered_Segmented_Customers_Analysis](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/53be6d93-7ad6-4642-894b-7e6419ec949a)


| Income & Spending Clusters | Age  | Annual Income (k$) | Spending Score (1-100) |
|----------------------------|------|--------------------|------------------------|
| 0                          | 32.69| 86.54              | 82.13                  |
| 1                          | 41.11| 88.20              | 17.11                  |
| 2                          | 25.27| 25.73              | 79.36                  |
| 3                          | 42.72| 55.30              | 49.52                  |
| 4                          | 45.22| 26.30              | 20.91                  |

The five clusters represent the following customer segments:

###### Cluster 0: Young High Spenders
  
###### Cluster 1: Older Conservative Spenders

###### Cluster 2: Young High Earners and Spenders

###### Cluster 3: Middle-Aged Conservative High Earners

###### Cluster 4: Moderate Earners and Spenders

The following provides detailed insights for each cluster, including age, annual income, spending scores, and gender distribution

_a) Cluster 0 (Young High Spenders):_

* Younger customers (average age around 25-30)
* Moderate income levels
* High spending scores

_b) Cluster 1 (Older Conservative Spenders):_
* Older customers (average age around 55-60)
* Higher-income levels
* Lower spending scores

_c) Cluster 2 (Young High Earners and Spenders):_
* Young to middle-aged customers (average age around 30-35)
* High-income levels
* High spending scores

_d) Cluster 3 (Middle-Aged Conservative High Earners):_
* Middle-aged customers (average age around 45-50)
* High-income levels
* Moderate spending scores
  
_e) Cluster 4 (Moderate Earners and Spenders):_
* Mixed age group (possibly spanning various age ranges)
* Moderate income levels
* Moderate spending scores


## Overall Insights:

### 1. High-income clusters with high spending scores <mark>(Cluster 2)</mark> should be targeted for premium and exclusive offers.

### 2. Younger, high-spending but low-income clusters <mark>(Cluster 4)</mark> can be attracted with affordable pricing and trendy products.

### 3. Balanced spenders and income <mark>(Cluster 1)</mark> can be targeted with value-for-money offers.

### 4. Older, low-income, low-spending clusters <mark>(Cluster 0)</mark> might need more basic and essential product offerings.

### 5. Older, high-income but low-spending clusters <mark>(Cluster 3)</mark> might appreciate premium quality over quantity.



### Multivariate Clustering:

![Clustered_MultivariatePlot_3DView](https://github.com/aishincp/CustomerSegmentation_DataScienceProject/assets/45165287/c15b8de9-d6dd-4e2a-badb-2bf829d923fd)

Based on the output of multivariate clustering, the derived insights are as follows:

**Cluster 0:**

Average Age: 25.25 years

Average Annual Income: $25.83k

Average Spending Score: 76.92

Gender Distribution:
Female: 41.67%
Male: 58.33%

_Insights:_

- This cluster has the youngest average age.
- They have the lowest average annual income.
- They have a high spending score, indicating they are enthusiastic spenders despite their lower income.
- Males are slightly more prevalent in this cluster.

**Cluster 1:**

Average Age: 54.06 years

Average Annual Income: $40.46k

Average Spending Score: 36.72

Gender Distribution:
Female: 44.00%
Male: 56.00%

_Insights:_

- This cluster has the oldest average age.
- Their average income is moderate.
- They have a lower spending score, suggesting they are conservative spenders.
- Males are more prevalent in this cluster.

**Cluster 2:**

Average Age: 32.69 years

Average Annual Income: $86.54k

Average Spending Score: 82.13

Gender Distribution:
Female: 46.15%
Male: 53.85%

_Insights:_

- This cluster has a younger average age compared to others.
- They have the highest average income.
- They also have the highest spending score, indicating high spending capability and behavior.
- There is a relatively balanced gender distribution, with a slight male majority.

**Cluster 3:**

Average Age: 41.65 years

Average Annual Income: $88.74k

Average Spending Score: 16.76

Gender Distribution:
Female: 55.88%
Male: 44.12%

_Insights:_

This cluster has a middle-aged average age.
They have a high average income.
They have the lowest spending score, indicating they are very conservative spenders.
Females are more prevalent in this cluster.

**Cluster 4:**

Average Age: 33.40 years

Average Annual Income: $58.06k

Average Spending Score: 48.77

Gender Distribution:
Female: 35.85%
Male: 64.15%

_Insights:_

This cluster has a slightly older average age than Cluster 2.
Their average income is moderate.
They have a moderate spending score.
Males are more prevalent in this cluster, with the highest male proportion among all clusters.


















  
