# Customer Segmentation Model

This project demonstrates a **Customer Segmentation** system using **K-Means Clustering**. Customer segmentation helps businesses group their customers based on shared characteristics, allowing for tailored marketing strategies, improved customer satisfaction, and enhanced revenue opportunities.

---

## Overview  
The model groups customers into clusters based on their purchasing behaviors and other key features. Using **K-Means Clustering**, we determine an optimal number of clusters, which best fits the data, helping to identify natural groupings among customers.

---

## Dataset Description  
The dataset includes various customer features such as spending habits, income, and other demographic information. Each feature contributes to identifying segments with distinct purchasing or engagement patterns.

### Key Features:
- **CustomerID**: Unique identifier for each customer
- **Gender**: Customer's gender
- **Age**: Age of the customer
- **Annual Income**: Estimated annual income of the customer
- **Spending Score**: Score assigned based on customer spending habits

---

## Methodology  

1. **Feature Extraction**: Extracted relevant features from the dataset needed for efficient clustering.
2. **Elbow Method**: Used the **Elbow Method** to find the optimal number of clusters. The elbow point on the plot indicates where the rate of decrease in **inertia** (within-cluster sum of squares) slows down, suggesting a good number of clusters.
3. **K-Means Clustering**: Applied **K-Means** with the optimal number of clusters found from the elbow method.

---

## Model Usage  

Below is an example of how to use this model to assign a new customer to a segment (this was not implemented in the actual code):

```python
import numpy as np

# Example customer data: (Annual Income, Spending Score)
customer_data = (70000, 60)

# Convert customer data to numpy array
customer_np = np.asarray(customer_data)

# Reshape data for clustering (single instance)
customer_reshaped = customer_np.reshape(1, -1)

# Predict the cluster
cluster = model.predict(customer_reshaped)

print(f"The customer belongs to segment: {cluster[0]}")
```

Feel free to use or modify this model for customer segmentation tasks. Suggestions and contributions are welcome!
