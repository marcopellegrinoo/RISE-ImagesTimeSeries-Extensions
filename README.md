# RISE-ImagesTimeSeries-Extensions

# RISE Extensions for Time-Series of Hydrological Images

This repository contains the implementation of various extensions of the Randomized Input Sampling for Explanation (RISE) method, tailored for **time-series of hydrological images**. The project is part of a Master's thesis on **Explainable Artificial Intelligence (XAI)**, focusing on providing saliency-based explanations for predictive models using image data in the hydrological domain.

## Table of Contents
- [Introduction](#introduction)
- [Methodology](#methodology)
- [Code Structure](#code-structure)
- [Examples](#examples)
- [Evaluation Metrics](#evaluation-metrics)
- [License](#license)

## Introduction
This project presents three experimental extensions of the RISE method designed to explain the predictions of machine learning models working on **time-series of images**. The images represent weather-related data (e.g., precipitation, temperature) and are used to predict groundwater levels.

The key methods implemented are:
- **Spatial-RISE**: Focuses on spatial perturbations in the images to generate saliency maps.
- **Temporal-RISE**: Introduces perturbations across the time axis to highlight time-dependent saliency.
- **SpatialTemporal-RISE**: Combines both spatial and temporal perturbations to generate spatiotemporal saliency videos.

The saliency maps and videos provide visual explanations of how different regions and times influence the model's predictions.

## Methodology
The core algorithm is based on the original RISE framework, with modifications to handle **spatial** and **temporal** perturbations of the input images. These extensions allow the generation of:
- Saliency maps (for **Spatial-RISE**)
- Temporal saliency vectors (for **Temporal-RISE**)
- Saliency videos (for **SpatialTemporal-RISE**)

Each method generates perturbations using **Gaussian noise** and evaluates how these perturbations impact the model's predictions. The result is a measure of the importance of different regions (spatial) and time steps (temporal).

For more detailed descriptions, refer to the article linked here: [Article PDF](link-to-article).

## Code Structure
The repository contains several Jupyter notebooks located in the `notebooks/` directory:

- **ST_RISE**: Contains the generic code skeleton for Spatial-Temporal RISE.
- **ST_RISE_Testing_Deletion** and **ST_RISE_Testing_Insertion**: These notebooks contain testing on the Vottignasco Test-Set, generating saliency videos for all instances. Additionally, they include Insertion/Deletion testing, along with plots showing the errors across all instances.
- **Spatial-RISE**: Implementation of the spatial component with testing, generating saliency maps for all instances in Vottignasco, along with Insertion/Deletion tests.
- **Temporal-RISE**: Similar to the Spatial-RISE notebook, but focusing on the temporal component, generating saliency vectors for the instances.
- **insertion&deletion_mean_Spatial_Temporal_ST_RISE**: Contains the mean saliency results (maps, vectors, videos) for Insertion/Deletion across all instances, as well as cumulative plots for the three components: space, time, and space-time.

## Evaluation Metrics
The evaluation metrics used in this project are adapted from the original RISE method to fit the context of **time-series of hydrological images**. The key metrics are:

- **Insertion**: Measures the change in model confidence as salient frames (temporal), pixels (spatial), or both (spatial-temporal) are added back.
- **Deletion**: Measures the impact on model confidence when salient frames (temporal), pixels (spatial), or both (spatial-temporal) are removed.

These metrics help quantify the importance of both spatial and temporal regions in the model's decision-making process, depending on the specific RISE extension being applied (Spatial, Temporal, or SpatialTemporal).


## License
This project is licensed under the MIT License. See the LICENSE file for details.

