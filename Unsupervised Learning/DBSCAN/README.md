# DBSCAN

## What is DBSCAN?
**Density-Based Spatial Clustering** is an unsupervised algorithm that:
- Groups dense data points into clusters
- Identifies outliers as noise
- Doesn't require pre-specifying cluster count
- Works well with non-spherical cluster shapes

### How It Works
1. **Core Points**: Points with >`min_samples` neighbors within `eps` radius
2. **Border Points**: Neighbors of core points but lack their own dense neighborhood
3. **Noise Points**: Points not reachable from any core point

## Dataset
### Big Five Inventory-2 Traits
- **Variables**: `openness`, `conscientiousness`, `extraversion`, `agreeableness`, `neuroticism`
- **Scale**: 12-60 per trait (12 items × 1-5 Likert)
- **Sample**: Typically N > 300 for stable clusters 

## Task
Predict dominant RIASEC personality types, the type with the highest value:
1. **Realistic (R)**
2. **Investigative (I)**
3. **Artistic (A)**
4. **Social (S)**
5. **Enterprising (E)** 
6. **Conventional (C)**

Using density patterns in psychological trait space.

## Key Insights
### Psychological Findings
-  **Artistic Types**: Most distinct cluster (high openness)
-  **Social Types**: Moderate separation (high extraversion+agreeableness)
-  **Challenges**: Conventional/Realistic often overlap

### ML Performance
| Metric          | Score  |
|-----------------|--------|
| Avg. Silhouette | 0.15-0.3 |
| Cluster Purity  | 25-40% |
| Noise Points    | 10-25% |
