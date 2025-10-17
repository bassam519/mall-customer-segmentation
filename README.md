# README.md

## Mall Customer Segmentation using K-Means Clustering 🛍️

---

### Project Overview and Core Idea

The modern retail environment demands highly personalized marketing strategies. A mall with a diverse customer base cannot effectively use a "one-size-fits-all" approach.

**The Project's Idea** is to solve this business challenge by applying **unsupervised machine learning** to transform raw transaction and demographic data into distinct, manageable customer segments. By understanding the intrinsic behavior and financial capacity of different groups, the mall can:

1.  **Optimize Marketing Spend:** Focus advertising budgets on the high-value segments (e.g., Target Group).
2.  **Product Recommendation:** Tailor product displays and inventory stocking based on segment preferences.
3.  **Customer Retention:** Develop specific loyalty programs and incentives for at-risk or high-potential customers.

This implementation uses **K-Means Clustering** to segment customers primarily based on their **Annual Income (k\$)** and their **Spending Score (1-100)**. This combination provides a powerful 2D view of a customer's financial ability versus their purchase frequency and value. The K-Means algorithm naturally discovers patterns in this data, identifying groups that might otherwise be overlooked.

---

### Key Features and Methodology

* **Business Problem to ML Task:** Converting the business need of "targeted marketing" into the ML task of "clustering."
* **Data Preparation:** Handled initial data cleaning, ensuring categorical features (like 'Gender') are appropriately addressed, though the primary clustering uses the two key numerical features.
* **Optimal Cluster Determination:** The **Elbow Method** was used as a diagnostic tool to statistically identify the ideal number of clusters (**k=5**) that minimize intra-cluster distance while maintaining clear separation.
* **K-Means Clustering:** Applied the model to create the final customer segments, defining the centroid (average profile) for each group.
* **Model Evaluation:** The quality of the discovered structure was validated using the **Silhouette Score**.

---

### Dataset

The project utilizes the **`Mall_Customers.csv`** dataset, containing critical features for segmentation:

| Column Name | Description |
| :--- | :--- |
| **CustomerID** | Unique ID assigned to the customer |
| **Gender** | Gender of the customer |
| **Age** | Age of the customer |
| **Annual Income (k\$)** | Annual income of the customer in thousands of dollars |
| **Spending Score (1-100)** | Score assigned by the mall based on customer behavior and spending nature (100 being the highest) |

---

### Results and Visualization

The K-Means algorithm successfully identified **5 distinct clusters** (segments), each representing a unique customer profile with clear strategic implications:

| Cluster | Profile Description | Strategic Marketing Focus |
| :--- | :--- | :--- |
| **1 (Target Group)** | High Income, High Spending (The Ideal Customer) | **Retention & Loyalty:** Offer exclusive premium products and personalized concierge services. |
| **2 (Cautious Group)** | Low Income, Low Spending | **Value & Promotions:** Use mass-market campaigns, budget-friendly bundles, and clear discount messaging. |
| **3 (High Spenders)** | Low Income, High Spending (High Potential) | **Encouragement:** Focus on sales volume, use store credit or limited-time offers to maintain spending momentum. |
| **4 (Miserly Group)** | High Income, Low Spending (High Value Potential) | **Engagement:** Focus on experience-based marketing, personalized outreach, and high-end niche product launches. |
| **5 (Mid-Range)** | Average Income, Average Spending | **Standard Offers:** Utilize general advertising and seasonal sales to capture mainstream market share. |

The visualization below shows the resulting clusters, with the 'X' markers denoting the center (centroid) of each distinct segment:

![K-Means Clustering Result](https://github.com/bassam519/mall-customer-segmentation/blob/main/Screenshot%202025-10-17%20122222.png)

### Model Performance

The clustering quality was assessed using the **Silhouette Score**:

$$\text{Silhouette Score: } \mathbf{0.5539}$$

This score of approximately $0.554$ is a strong indicator that the clusters are both **internally cohesive** (customers within a cluster are similar) and **externally separated** (clusters are distinct from one another), validating the segmentation as reliable and actionable.

---

### Technologies and Libraries

This project is implemented in **Python** and requires the following libraries:

* `pandas` (Data manipulation)
* `numpy` (Numerical operations)
* `matplotlib` & `seaborn` (Data visualization)
* `scikit-learn` (`sklearn`) (K-Means algorithm and Silhouette Score)

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
    Open and execute the cells in the Jupyter Notebook: `Customer Segmentation Using Machine Learning.ipynb` to reproduce the analysis and results.
    ```bash
    jupyter notebook "Customer Segmentation Using Machine Learning.ipynb"
    ```
