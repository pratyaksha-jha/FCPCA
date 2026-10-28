# FCPCA: EEG Signal Clustering
This project uses Fuzzy Clustering of Multivariate Time Series based on PCA (FCPCA) to group EEG signals into alert, drowsy, and mixed/transitional states.
- **Course**: DA3011L
- **Author**: Pratyaksha Jha, Somita Agarwal
- **Roll No**: 240150025, 240150035
## Dataset
- The dataset file is `dataset.mat`.
- It contains 2,022 EEG samples from 11 subjects.
- Each sample contains 30 EEG channels recorded over 384 time points.
- The labels identify the subject and the alert/drowsy state.

## Workflow
1. Load and organize the EEG data by subject.
2. Normalize the EEG samples.
3. Calculate covariance matrices for time lags 1 and 2.
4. Use PCA to retain components explaining 95% of the variance.
5. Run FCPCA with two clusters.
6. Use the Xie-Beni and Fuzzy Silhouette indices to search for a suitable fuzziness value.
7. Identify mixed/transitional states using a membership threshold of 0.7.
8. Evaluate the results using Rand Index (RI) and Adjusted Rand Index (ARI).
9. Plot membership values and summary results.
## Output
The notebook displays clustering scores for each subject, the number of detected mixed/transitional states, and plots showing the membership values and overall results.
## Reference
The implementation is based on the FCPCA research paper:
https://www.sciencedirect.com/science/article/pii/S0888613X25001938
