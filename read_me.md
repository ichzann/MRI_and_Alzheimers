# Alzheimer's Detection & Trajectory Modeling Using PCA / UMAP Projections

While learning about dimension reduction methods (PCA and UMAP), I realized that in a well-separated PCA space, the representation of an individual data point over time could effectively visualize disease progression.

To test this, I trained an LSTM model designed to predict two things simultaneously:

The future coordinates of a patient in the reduced PCA / UMAP latent space.

The clinical grouping (demented vs. non-demented) of that data point.

Key Finding: Implementing PCA instead of UMAP proved to be much more effective for this time-series forecasting. This is likely because PCA preserves global, linear distance attributes, whereas UMAP creates a warped, non-linear topological space. Furthermore, compared to raw PCA, Supervised PCA seems to be better  at clearly separating the data points.

# AI Use
I utilized AI tools during this project to help generate plotting scripts, assist with tensor shape mismatches, and refine the architecture of the LSTM. And of course I created this readme with AI 