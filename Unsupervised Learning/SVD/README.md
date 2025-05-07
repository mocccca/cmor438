## 1. Image Compression using Singular Value Decomposition (SVD)

### What is Singular Value Decomposition?
Singular Value Decomposition (SVD), a matrix factorization technique to compress lossy images. Through breaking down an image into three matrices (U, Σ, Vᵀ), it retain only the most important singular values, thus reducing storage size while maintaining reasonable visual quality.

### How It Works:
1. **SVD Definition**:
   Singular Value Decomposition (SVD) decomposes any matrix A (in this case, an image) into three matrices: A=UΣVᵀ
Where:
- U: Left singular vectors (orthogonal matrix, represents "row space").
- Σ: Diagonal matrix of singular values (sorted in descending order).
- Vᵀ: Right singular vectors (orthogonal matrix, represents "column space").

2. **SVD in Image Compression**:
- The singular values (Σ) indicate the "importance" of each component.
- Keeping only the top k singular values (and setting the rest to zero) gives a compressed approximation: A=U<sub>k</sub>Σ<sub>k</sub>V<sub>k</sub>ᵀ
- The higher k, the better the quality, but the lower the compression.

### 2. Data & task


