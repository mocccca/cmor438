# K-means Clustering

## What is K-means Clustering?
**Definition:** An unsupervised machine learning algorithm that partitions data into K distinct clusters based on feature similarity.

**How It Works:**
1. Randomly initialize K cluster centroids
2. Assign each point to nearest centroid
3. Recalculate centroids as cluster means
4. Repeat until convergence

## Dataset
- **Variables:** 
  - 20 leisure activity scores (LIQ)
  - 6 RIASEC personality scores 
  - Derived dominant RIASEC type
- **Sample Size:** 121 participants

## Analysis Task
1. Cluster participants based on leisure activities
2. Compare clusters to actual RIASEC types
3. Identify which activities best predict personality types

## Key Insights
### Cluster Characteristics
- **Artistic Types:** Most distinct cluster (55% purity)
  - High cultural arts/literature engagement
- **Social-Conventional Blend:** Hard to distinguish
  - Shared preference for socializing/group activities
- **Missing Types:** Realistic/Enterprising poorly captured

### Psychological Implications
- Leisure activities strongly signal artistic personality
- Social/conventional types share similar activity profiles
- Need additional measures for hands-on/enterprising types
