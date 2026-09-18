# 👜👟 Handbags vs. Shoes Image Classifier

## 💼 Business use case

E-commerce teams spend a surprising amount of time cleaning product catalogs and correcting image labels. A lightweight visual classifier can handle the obvious cases automatically, route images to the right category, and leave uncertain examples for manual review. This project explores that idea in a deliberately small-data setting, where fewer than 100 training images are available.

## 🎯 Principal objective

Build a binary image classifier for **handbags and shoes** and understand how modeling choices affect performance when labeled data is scarce. The notebook compares a small convolutional neural network, the same architecture with data augmentation, and transfer learning with ResNet50.

## 🔎 Summary of takeaways

The progression across the three experiments is clear: the baseline CNN reaches **72.5% test accuracy** with **1.0832** loss, augmentation improves it to **72.5%** with **0.6510** loss, and the ResNet50-based approach reaches **97.5%** with **0.7530** loss on the stored test set. The result illustrates why transfer learning is often the practical choice for small image datasets: pretrained visual features provide a much stronger starting point than learning every representation from scratch.

The strongest score should still be interpreted carefully because the test set contains only 40 images. In a production catalog, I would validate the model on a larger independent sample, evaluate confidence calibration, and test harder examples with varied backgrounds, lighting, occlusion, and product styles.

## 🧭 Explore the code

The [notebook](https://github.com/saels/handbag-shoes-classifier/blob/3994369cf4444bbbeecaf49a4da00e157417bf36/Handbags_shoes_classifier.ipynb) walks through image preparation, CNN training, augmentation, transfer learning, and model comparison. Check the code to see how each approach changes the learning problem and why the pretrained model performs best in this small-data scenario.
