# AdversarialAttacksDL

This repository contains code examples and implementations of adversarial attacks targeting deep learning models, including evasion and poisoning attacks. The implementations utilize the Adversarial Robustness ToolBox (ART) framework.

## Overview

This project consists of three main parts:

1. **Model Construction**: Building a deep learning model to classify malware families based on their images.
2. **Adversarial Attacks**: Investigating and implementing various adversarial attacks using the ART framework.
3. **Defensive Techniques**: Implementing and evaluating defensive techniques to mitigate the impact of adversarial attacks.

## Model Construction

In the first part of the project, a deep learning model was constructed to classify malware families using their images. The model was trained on a dataset consisting of images of different malware families.

![Malware Families](MalimgImage.png)

## Adversarial Attacks

**Test accuracy of original model**: 0.9625

### Poisoning Attack

- **Test accuracy of poisoned model**: 0.0442

A poisoning attack was carried out by injecting malicious samples into the training data, severely degrading the model's performance.

### Evasion Attack

- **Accuracy on adversarial samples**: 0.0242

An evasion attack using the Fast Gradient Method (FGM) was conducted to create adversarial examples that fool the model into making incorrect predictions.

## Defensive Techniques

### Defense against Poisoning

- **Test accuracy of defended model**: 0.3291

A defense mechanism involving JPEG compression was implemented to mitigate the effects of poisoning. While this defense improved the accuracy significantly compared to the poisoned model, there is still room for further improvement.

### Defense against Evasion

- **Accuracy of model with adversarial training on clean samples**: 0.7231
- **Accuracy of model with adversarial training on adversarial samples**: 0.6820

Adversarial training was used to defend against evasion attacks. This technique improved the model's robustness, maintaining reasonable accuracy on both clean and adversarial samples.

## Acknowledgements

This project was developed as part of the "Security Data Science" course and was inspired by the following sources and references:

- Goodfellow, I., Shlens, J., & Szegedy, C. (2014). Explaining and Harnessing Adversarial Examples. arXiv (Cornell University). [Link](https://doi.org/10.48550/arxiv.1412.6572)
- Biggio, B., Nelson, B. D., & Laskov, P. (2012). Poisoning Attacks against Support Vector Machines. arXiv (Cornell University). [Link](https://doi.org/10.48550/arxiv.1206.6389)
