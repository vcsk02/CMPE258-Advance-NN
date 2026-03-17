# Video Script - Notebook 05 Time Series, Tabular, Speech, and Document Images

Open by saying this notebook finishes the multimodal augmentation requirements.

Walkthrough order:
1. Time series:
   - explain sine vs square wave classification
   - jitter, scaling, and shifting
   - 1D CNN baseline vs augmented
2. Tabular:
   - explain why tabular augmentation must be careful
   - show interpolation between minority-class samples plus mild noise
   - compare MLP baseline vs augmented data
3. Speech:
   - explain synthetic tone classes
   - convert signals to spectrograms
   - add shift and noise augmentations
   - train the CNN on spectrograms
4. Document images:
   - explain invoice vs memo templates
   - show scan-like corruption: blur, rotation, noise
   - compare baseline vs augmented
5. End by emphasizing that augmentation has to respect domain structure.

Closing line:
The lesson here is that augmentation is powerful only when the transformed samples still make semantic sense for the task.
