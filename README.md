# CMPE258 - Advanced Neural Networks Assignment Repo

This repository is organized as a **multi-Colab submission** for the advanced neural networks assignment.  
The work is split into focused notebooks so each topic is easier to run, explain on video, and review on GitHub.

The design goals for this repo were simple:

- keep each notebook runnable in **Google Colab**
- cover the required topics in **both TensorFlow/Keras and PyTorch**
- include **A/B tests** instead of one-off demos
- make the code easy to narrate in a screen recording
- keep the repo clean enough that a grader can find things without archaeological tools

---

## Repository layout

```text
CMPE258-Advance-NN/
├── README.md
├── requirements.txt
├── .gitignore
├── part1/
│   ├── 01_tensorflow_regularization_abtests.ipynb
│   ├── 02_pytorch_regularization_abtests.ipynb
│   ├── 03_keras_tuner_and_keras_cv.ipynb
│   ├── 04_image_video_text_augmentation.ipynb
│   └── 05_timeseries_tabular_speech_document_augmentation.ipynb
├── part2/
│   ├── 06_advanced_keras_custom_objects.ipynb
│   ├── 07_advanced_pytorch_constructs.ipynb
│   └── 08_wandb_experiment_tracking.ipynb
└── video_scripts/
    ├── 01_tensorflow_regularization_abtests.md
    ├── 02_pytorch_regularization_abtests.md
    ├── 03_keras_tuner_and_keras_cv.md
    ├── 04_image_video_text_augmentation.md
    ├── 05_timeseries_tabular_speech_document_augmentation.md
    ├── 06_advanced_keras_custom_objects.md
    ├── 07_advanced_pytorch_constructs.md
    └── 08_wandb_experiment_tracking.md
```

---

## What is covered

## Part 1 - Data augmentation and generalization

### Notebook 1 - TensorFlow/Keras regularization A/B tests
Covers:

- L1 and L2 regularization
- dropout
- early stopping
- Monte Carlo dropout
- weight initialization comparisons
- batch normalization
- custom dropout layer
- custom regularizer
- callbacks
- TensorBoard logging

### Notebook 2 - PyTorch regularization A/B tests
Covers PyTorch versions of:

- weight decay / L2
- manual L1 penalty
- dropout
- batch normalization
- early stopping
- custom dropout module
- initialization experiments
- Monte Carlo dropout
- TensorBoard logging with `SummaryWriter`

### Notebook 3 - KerasTuner and KerasCV
Covers:

- hyperparameter search with KerasTuner
- search spaces for CNN depth, width, dropout, and learning rate
- KerasCV-style vision augmentation layers
- A/B comparison between plain preprocessing and stronger augmentation policy

### Notebook 4 - Image, video, and text augmentation
Covers:

- image augmentation and classification
- synthetic video augmentation and lightweight video classification
- text augmentation with `nlpaug`
- A/B comparisons between original training data and augmented training data

### Notebook 5 - Time series, tabular, speech, and document-image augmentation
Covers:

- time-series augmentation with jitter, scaling, and window slicing
- tabular augmentation with interpolation and noise injection
- speech augmentation with time shift and additive noise
- document image augmentation with blur, rotation, and scan-style corruption
- compact classification demos for each modality

---

## Part 2 - Advanced Keras and advanced PyTorch constructs

### Notebook 6 - Advanced Keras custom objects
Covers:

- custom learning-rate scheduler
- custom dropout
- custom normalization
- TensorBoard
- custom loss function
- custom activation
- custom initializer
- custom regularizer
- custom kernel constraint
- custom metric
- custom layers
- custom model
- custom optimizer
- custom training loop

### Notebook 7 - Advanced PyTorch constructs
Covers:

- custom dataset and transforms
- custom scheduler
- custom dropout module
- custom normalization layer
- custom loss and metric logic
- residual model block
- custom optimizer implementation
- explicit training loop
- TensorBoard integration
- post-step weight constraints

### Notebook 8 - Weights & Biases experiment tracking
Covers:

- W&B setup
- run configuration logging
- metric logging
- model checkpoint logging
- confusion matrix logging
- artifact logging
- a compact training example suitable for demo on video

---

## How to run in Colab

Open each notebook in Google Colab and run the cells top to bottom.

Recommended order:

1. `part1/01_tensorflow_regularization_abtests.ipynb`
2. `part1/02_pytorch_regularization_abtests.ipynb`
3. `part1/03_keras_tuner_and_keras_cv.ipynb`
4. `part1/04_image_video_text_augmentation.ipynb`
5. `part1/05_timeseries_tabular_speech_document_augmentation.ipynb`
6. `part2/06_advanced_keras_custom_objects.ipynb`
7. `part2/07_advanced_pytorch_constructs.ipynb`
8. `part2/08_wandb_experiment_tracking.ipynb`

### Colab notes

- Choose **GPU runtime** for the CNN notebooks.
- The multimodal notebooks use **small datasets or synthetic data** to keep execution practical in Colab.
- Some augmentation libraries are installed inside the notebook with `pip`.
- W&B requires login if online tracking is enabled.

---

## Video walkthrough plan

The assignment requires a video explanation of each Colab.  
Since each notebook already contains markdown sections, the easiest recording flow is:

1. Start with the notebook goal and dataset.
2. Explain imports and helper utilities.
3. Walk through the model-building code.
4. Explain the augmentation or custom-object section.
5. Run training cells and comment on metrics.
6. Show TensorBoard or W&B outputs where applicable.
7. End with a brief comparison: baseline vs augmented / custom version.

Detailed speaking notes are provided in the `video_scripts/` folder.

---

## Suggested GitHub upload flow

```bash
git clone https://github.com/vcsk02/CMPE258-Advance-NN.git
cd CMPE258-Advance-NN

# copy the generated files into the repo
git add .
git commit -m "Add multi-colab advanced neural network assignment"
git push origin main
```

---

## Suggested README additions after you record videos

After uploading your videos, add a section like this near the top of the README:

```md
## Video Walkthroughs

- Notebook 1 walkthrough: <YouTube or Drive link>
- Notebook 2 walkthrough: <YouTube or Drive link>
- Notebook 3 walkthrough: <YouTube or Drive link>
- Notebook 4 walkthrough: <YouTube or Drive link>
- Notebook 5 walkthrough: <YouTube or Drive link>
- Notebook 6 walkthrough: <YouTube or Drive link>
- Notebook 7 walkthrough: <YouTube or Drive link>
- Notebook 8 walkthrough: <YouTube or Drive link>
```

---

## What still needs your manual action

This package gives you the **repo content**.  
You still need to do three human things:

1. run each notebook in Colab and save the outputs
2. record the walkthrough videos
3. paste your final public video links into this README

I cannot directly upload files or videos to your GitHub from here, so I built the repo structure and narration material for you instead.

---

## Why the notebooks are split up this way

One giant notebook would be a swamp creature.  
Splitting the work makes it easier to:

- keep runtimes manageable
- isolate package installs
- debug failed cells
- explain code clearly during the video
- show the grader a clean mapping from rubric item to notebook section

---

## Rubric mapping summary

| Requirement | Notebook |
|---|---|
| TensorFlow regularization + callbacks + TensorBoard | 01 |
| PyTorch regularization + TensorBoard | 02 |
| KerasTuner | 03 |
| KerasCV augmentation | 03 |
| Image / video / text augmentation | 04 |
| Time-series / tabular / speech / document augmentation | 05 |
| Advanced Keras custom objects | 06 |
| Advanced PyTorch constructs | 07 |
| Weights & Biases | 08 |

---

## Reference inspiration used while designing the topics

These notebooks were written fresh for this repo, but the topic coverage is aligned with the assignment references such as:

- Géron deep-learning notebooks on training neural networks and custom models
- TensorFlow image augmentation tutorials
- KerasTuner documentation
- KerasCV / Keras augmentation docs
- AugLy for multimodal augmentation
- `nlpaug` for text augmentation
- W&B docs for experiment tracking

The implementations here are intentionally rewritten in a repo-friendly style for this assignment instead of copying the referenced notebooks.

---
