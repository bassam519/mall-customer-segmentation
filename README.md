# README.md

## Mall Customer Segmentation using K-Means Clustering 🛍️

---

### Project Overview

This project implements an **unsupervised machine learning** technique, **K-Means Clustering**, to segment mall customers into distinct groups based on their spending habits and income. The goal is to provide actionable insights for the mall's marketing team to develop targeted strategies for each segment, optimizing resource allocation and maximizing revenue.

The analysis is performed primarily on two critical features: **Annual Income (k\$)** and **Spending Score (1-100)**.

---

### Key Features

* **Data Preprocessing:** Handled categorical data (like 'Gender') and ensured numerical features were ready for clustering.
* **Exploratory Data Analysis (EDA):** Visualizing distributions of key features such as Annual Income, Spending Score, and Age to understand underlying patterns.
* **Optimal Cluster Determination:** Utilized the **Elbow Method** (or similar analysis) to determine the ideal number of clusters (**k**), which in this analysis was determined to be 5.
* **K-Means Clustering:** Applied the K-Means algorithm to create the final customer segments.
* **Model Evaluation:** Evaluated the model's performance and cluster quality using the **Silhouette Score**.

---

### Dataset

The project utilizes the **`Mall_Customers.csv`** dataset, which contains customer information with the following attributes:

| Column Name | Description |
| :--- | :--- |
| **CustomerID** | Unique ID assigned to the customer |
| **Gender** | Gender of the customer |
| **Age** | Age of the customer |
| **Annual Income (k\$)** | Annual income of the customer in thousands of dollars |
| **Spending Score (1-100)** | Score assigned by the mall based on customer behavior and spending nature (100 being the highest) |

---

### Results and Visualization

The K-Means algorithm successfully identified **5 distinct clusters** that represent different customer segments:

| Cluster | Description | Marketing Strategy Focus |
| :--- | :--- | :--- |
| **1 (Target Group)** | High Income, High Spending | **Retention & Loyalty:** Offer exclusive premium products and services. |
| **2 (Cautious Group)** | Low Income, Low Spending | **Value & Promotions:** Offer budget-friendly deals and heavy discounts. |
| **3 (High Spenders)** | Low Income, High Spending | **Encouragement:** Offer store credit or targeted offers to increase average transaction value. |
| **4 (Miserly Group)** | High Income, Low Spending | **Engagement:** Focus on lifestyle products, personalized recommendations, and experience-based marketing. |
| **5 (Mid-Range)** | Average Income, Average Spending | **Standard Offers:** Use broad campaigns and regular seasonal sales. |

The visualization below shows the resulting clusters, with the 'X' markers denoting the cluster centroids:

![K-Means Clustering Result](https://github.com/bassam519/mall-customer-segmentation/blob/main/Screenshot%202025-10-17%20122222.png)

### Model Performance

The clustering quality was assessed using the **Silhouette Score**:

$$\text{Silhouette Score: } \mathbf{0.5539}$$

A score of approximately $0.554$ is generally considered **good**. This indicates that the clusters are reasonably **dense** (members within a cluster are similar) and **well-separated** (clusters are distinct from each other), confirming the reliability of the customer segments found.

---

### Technologies and Libraries

This project is implemented in **Python** and requires the following libraries:

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn` (`sklearn`)

---

### Installation and Setup

1.  **Clone the Repository:**
    ```bash
    git clone [Your Repository URL]
    cd mall-customer-segmentation
    ```

2.  **Install Required Libraries:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn jupyter
    ```

3.  **Run the Analysis:**
    Open and execute the cells in the Jupyter Notebook: `Customer Segmentation Using Machine Learning.ipynb`.
    ```bash
    jupyter notebook "Customer Segmentation Using Machine Learning.ipynb"
    ```
