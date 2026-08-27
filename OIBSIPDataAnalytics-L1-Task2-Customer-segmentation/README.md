import numpy as np
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

# 1. Prepare and scale the RFM data
# Standardizing features (Recency, Frequency, Monetary) is required for K-Means 
# to ensure high-magnitude features (Monetary) do not dominate the distance metrics.
X = rfm[['Recency', 'Frequency', 'Monetary']].values
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# 2. Compute Within-Cluster Sum of Squares (WCSS) for K values ranging from 1 to 10
wcss = []
K_range = range(1, 11)

for k in K_range:
    kmeans = KMeans(n_clusters=k, random_state=42, n_init=10)
    kmeans.fit(X_scaled)
    wcss.append(kmeans.inertia_)

# 3. Plot the Elbow Method curve
plt.figure(figsize=(10, 6))
plt.plot(K_range, wcss, marker='o', linestyle='--', color='b', linewidth=2, markersize=8)
plt.title('Elbow Method for Optimal Number of Clusters (K)', fontsize=14, fontweight='bold', pad=15)
plt.xlabel('Number of Clusters (K)', fontsize=12)
plt.ylabel('Within-Cluster Sum of Squares (WCSS / Inertia)', fontsize=12)
plt.xticks(K_range)
plt.grid(True, linestyle=':', alpha=0.6)
plt.show()

# 4. Independent step-by-step verification of WCSS values
print("=== WCSS VALUES PER CLUSTER (K) ===")
for k, inertia in zip(K_range, wcss):
    print(f"K = {k:2d} | WCSS = {inertia:10.2f}") 

Observation & Recommendation:
Look for the "elbow point" in the generated plot where the rate of decrease in WCSS sharply slows down (typically $K = 3$ or $K = 4$ for standard RFM customer segmentation). Selecting $K = 3$ or $K = 4$ balances model compactness with customer group interpretability.