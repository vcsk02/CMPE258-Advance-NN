# Video Script - Notebook 04 Image, Video, and Text Augmentation

Open by saying this notebook shows that augmentation is a cross-modal idea, not just a vision trick.

Walkthrough order:
1. Start with the image section:
   - CIFAR-10 subset
   - KerasCV augmenter
   - small CNN
   - baseline vs augmented comparison
2. Move to the video section:
   - explain the synthetic moving-square dataset
   - show how horizontal vs vertical motion creates a simple classification task
   - explain video augmentation with noise, brightness, and crop
   - point out the 3D CNN
3. Move to the text section:
   - explain the small sentiment dataset
   - show `nlpaug` synonym augmentation
   - explain TF-IDF + logistic regression as a lightweight baseline
4. Show the before/after augmentation examples for images and text.
5. Summarize the baseline vs augmented results.

Closing line:
Different modalities use different transformations, but the shared goal is always the same: train on a richer distribution so the model becomes less brittle.
