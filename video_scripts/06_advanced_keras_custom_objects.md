# Video Script - Notebook 06 Advanced Keras Custom Objects

Open by saying this notebook collects advanced Keras extension points in one place.

Walkthrough order:
1. Explain the synthetic regression dataset.
2. Walk through custom activation, initializer, regularizer, and constraint.
3. Explain `CustomMCDropout` and `FeatureMaxNorm`.
4. Explain custom loss and metric:
   - SmoothHuberLoss
   - HuberMetric
5. Explain custom layers:
   - ExponentialLayer
   - AddGaussianNoise
   - LayerNormalizationLite
   - MyDense
6. Explain `ResidualBlock` and `ResidualRegressor`.
7. Explain `SimpleMomentumOptimizer`.
8. Explain `OneCycleStyleScheduler`.
9. Show compile + fit + TensorBoard callback.
10. Show MC dropout uncertainty.
11. Move to the custom training loop section and explain `tf.GradientTape`.

Closing line:
Keras is flexible enough that when built-in pieces are not enough, you can extend almost every part of the training stack yourself.
