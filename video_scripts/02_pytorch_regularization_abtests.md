# Video Script - Notebook 02 PyTorch Regularization A/B Tests

Open by saying this notebook recreates the same regularization study in PyTorch.

Walkthrough order:
1. Imports, device selection, and seed setting.
2. Show FashionMNIST loaders.
3. Explain `StochasticScaleDropout` and the `MLP` class.
4. Explain initialization choices in `initialize_weights(...)`.
5. Explain L1 vs L2 in PyTorch:
   - L2 via `weight_decay`
   - L1 added manually to the loss
6. Walk through `train_model(...)`:
   - optimizer
   - SummaryWriter
   - validation tracking
   - early stopping logic
7. Run experiment configs and compare results.
8. Show the validation accuracy chart.
9. Explain Monte Carlo dropout by keeping dropout layers in train mode at inference.
10. Show the TensorBoard log directory.

Closing line:
The PyTorch version proves the ideas transfer across frameworks even though the implementation style is different.
