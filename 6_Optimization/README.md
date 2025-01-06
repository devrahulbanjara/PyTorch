# Preventing Overfitting

Overfitting occurs when a model performs well on training data but poorly on unseen data. Here's how to address it:

- **Add More Data**: If feasible, more data can improve generalization.
- **Data Augmentation**: Enhance limited data by applying transformations.
- **Weight Decay**: Penalize large weights to maintain simplicity.
- **Simplify Model**: Reduce model complexity to avoid overfitting.
- **Batch Normalization**: Stabilize and regularize training.
- **Early Stopping**: Stop training when validation performance degrades.
- **Dropout**: Randomly deactivate neurons to prevent co-adaptation.

Combine these techniques for a more robust and generalizable model.