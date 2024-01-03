Kthperclass Classifier

Introduction

The kthperclass classifier is a tool designed to categorize test feature vectors by leveraging a set of training feature vectors accompanied by associated labels. Governed by a crucial parameter "k," denoting the number of training vectors per class, this classifier operates with a distinct distance metric and employs tie-breaking rules. Notably, for k=1, it seamlessly aligns with the k-nearest-neighbor (kNN) classifier.

Classifier Description

In the vein of the kNN classifier, the kthperclass variant identifies the k nearest neighbors for each class. The figure-of-merit (FOM) is determined based on the distance to the kth nearest neighbor for each class. The pivotal decision-making process hinges on selecting the class with the smallest FOM, ultimately defining the detected class.

Distance Metric

The chosen distance metric is the "Manhattan" or "cityblock" metric, represented as 𝑑𝑐(𝐱, 𝐲) = |𝑥1− 𝑦1| + |𝑥2− 𝑦2| + ⋯ + |𝑥ℓ− 𝑦ℓ|. This metric, tailored for length-2 vectors like [4.2 1.1] and [4.0 1.4], offers ease of computation.

Breaking Ties

To address tie scenarios, the "smallest" rule is strategically implemented. This rule allocates the tie to the class boasting the smallest index, a pragmatic solution that ensures clarity in classification outcomes.

This project was undertaken as part of the ECE759 Pattern Recognition course, instructed by Professor Greg Bottemly.
