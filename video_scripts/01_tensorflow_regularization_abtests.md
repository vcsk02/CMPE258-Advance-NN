# Video Script - Notebook 01 TensorFlow/Keras Regularization A/B Tests

Open by saying this notebook compares several generalization techniques on Fashion-MNIST in TensorFlow/Keras.

Walkthrough order:
1. Explain imports, seed setting, and why reproducibility matters.
2. Show the dataset split: train, validation, test.
3. Explain the three custom objects:
   - `MCDropout`
   - `StochasticScaleDropout`
   - `ActivationEnergyRegularizer`
4. Walk through `build_model(...)` and explain how flags toggle batch norm, dropout, initializers, and regularizers.
5. Explain `fit_experiment(...)`:
   - optimizer
   - early stopping
   - ReduceLROnPlateau
   - TensorBoard callback
6. Run the A/B experiment dictionary and explain baseline vs L1/L2 vs dropout vs batch norm.
7. Show the validation accuracy plot.
8. Explain initialization comparison:
   - He for ReLU
   - Glorot as a broad default
   - LeCun for self-normalizing settings
9. Explain Monte Carlo dropout and why repeated stochastic passes estimate uncertainty.
10. End by showing the TensorBoard log path.

Closing line:
This notebook shows that regularization is not one trick; it is a whole toolbox for controlling overfitting and improving robustness.
