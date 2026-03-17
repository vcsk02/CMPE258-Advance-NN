# Video Script - Notebook 03 KerasTuner and KerasCV

Open by saying this notebook covers two things: tuning the model and strengthening the data pipeline.

Walkthrough order:
1. Imports and package setup.
2. Explain why CIFAR-10 is reduced to a smaller subset for Colab practicality.
3. Show the augmentation visualization cell with `RandAugment` and cutout.
4. Explain plain dataset vs augmented dataset creation.
5. Walk through `build_tunable_model(hp)`:
   - blocks
   - filters
   - dense units
   - dropout
   - learning rate
6. Explain the `Hyperband` tuner and why it is a practical search strategy.
7. Run the search and show the best hyperparameters.
8. Rebuild the best model and train it on:
   - plain data
   - augmented data
9. Compare test results and explain why augmentation and tuning solve different parts of the problem.

Closing line:
Architecture search and augmentation are complementary; one changes the learner, the other changes what the learner sees.
