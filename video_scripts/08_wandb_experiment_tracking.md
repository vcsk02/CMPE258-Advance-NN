# Video Script - Notebook 08 Weights & Biases Experiment Tracking

Open by saying this notebook demonstrates experiment tracking rather than a fancy model.

Walkthrough order:
1. Explain online vs offline W&B mode.
2. Show the `config` dictionary and why logging hyperparameters matters.
3. Explain `wandb.init(...)`.
4. Walk through the model and data setup.
5. Show `wandb.watch(model)` and explain parameter / gradient tracking.
6. Walk through the training loop:
   - batch loss logging
   - epoch-level train and validation metrics
7. Show test evaluation.
8. Explain confusion matrix logging with `wandb.plot.confusion_matrix`.
9. Explain artifact logging for `best_model.pt`.
10. Show how to finish the run and sync offline runs later.

Closing line:
W&B turns a plain training loop into a traceable experiment, which matters a lot once you start comparing many runs.
