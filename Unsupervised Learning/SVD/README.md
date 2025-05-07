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

Uploaded two photos - a photo of the night view of the riverside along my city and a photo of me. 
1. Normalize and check channels, and apply SVD to each channel
2. Visualize results, based on different k levels (e.g., 50, 20, 10, 5)
3. Calculate compression ratio

### Key Insights

- SVD is an effective method for lossy image compression.
- Higher k = better quality but lower compression.
- Works well for landscapes, though fine details may blur at high compression. k cannot be too low for human potraits though.

