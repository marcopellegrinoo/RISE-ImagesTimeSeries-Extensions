# RISE-ImagesTimeSeries-Extensions

# RISE Extensions for Time-Series of Hydrological Images

This repository contains the implementation of various extensions of the Randomized Input Sampling for Explanation (RISE) method, tailored for **time-series of hydrological images**. The project is part of a Master's thesis on **Explainable Artificial Intelligence (XAI)**, focusing on providing saliency-based explanations for predictive models using image data in the hydrological domain.

## Table of Contents
- [Introduction](#introduction)
- [Methodology](#methodology)
- [Installation](#installation)
- [Usage](#usage)
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

For more detailed descriptions, refer to the thesis document linked here: [Article PDF](link-to-thesis).
