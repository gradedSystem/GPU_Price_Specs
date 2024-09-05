---
datapackage:
  title: GPU Price Dataset
  created: 2024-09-03
  updated: 2024-09-03
  format: csv
  sources:
    - path: https://pcbuilder.net/product/graphics-card/
      title: PC Builder Graphics Card
  resources:
    - name: gpu-price-dataset
      title: GPU Specs and Latest Prices
      description: |
        This dataset contains over 300 listed GPUs, video cards, and graphics cards with specifications and the latest prices. The data was scraped from the web database Pcbuilder. Note that only items with visible prices were included. The dataset is based on United States prices, so the prices are in US Dollars (USD).
      lastModified: 2024-09-03
      path: gpu_specs_prices.csv
    - name: NVIDIA-price-forecast
      title: NVIDIA Price Forecast in US
      description: |
        This dataset provides a forecast of NVIDIA GPU prices based on Statista projections. It covers the anticipated price trends for NVIDIA GPUs from 2024 to 2029.
      lastModified: 2024-09-05
      path: NVIDIA_PRICE.csv
---

# GPU Dataset Analysis

## Overview

This dataset offers a thorough examination of various GPUs, focusing on performance metrics across different APIs and detailed specifications. The analysis aims to facilitate comparisons between GPU performance and value based on benchmarks and pricing. It encompasses a range of GPUs, providing insights into their strengths and weaknesses in various contexts.

## Data Sections

### 1. GPU Performance Metrics

This section details the performance metrics of GPUs across several APIs, including CUDA, Metal, OpenCL, and Vulkan. Understanding these metrics is essential for evaluating how well different GPUs perform under various computational environments.

<FlatUiTable
  data={{
    url: 'GPU_scores_graphicsAPIs.csv'
  }}
/>

#### Key Insights

- **CUDA Performance**: The GeForce RTX 3090 Ti and the A100 series emerge as top performers in CUDA, showcasing exceptional computational power suitable for demanding tasks such as deep learning and complex simulations.
- **API Versatility**: NVIDIA GPUs, including the RTX 3090 and 3080 series, show strong performance across OpenCL and Vulkan APIs, indicating their robustness and adaptability for a wide range of applications, from gaming to professional graphics work.

### 2. GPU Specifications

This section includes detailed information on GPU benchmark scores, pricing, power consumption (TDP), and other critical specifications. These details help in assessing the overall value and suitability of different GPUs based on specific needs and budget constraints.


#### Key Insights

- **Benchmark Scores**: The GeForce RTX 3090 Ti achieves the highest G3Dmark score, reflecting its superior graphical performance. The RTX 3080 Ti and RTX 3090 also rank highly, making them strong candidates for high-end gaming and content creation.
- **Pricing and Value**: High-end GPUs like the RTX A6000 and Titan RTX come with premium prices, while models such as the RTX 3070 offer excellent performance at a more accessible cost. This allows for more flexibility in choosing a GPU that fits both performance needs and budget.
- **Power Consumption**: GPUs with higher TDP ratings, such as the RTX 3090 Ti, require significant power, which is an important consideration for system integration and efficiency. Ensuring that your power supply can handle these demands is crucial for maintaining system stability.

## Data Visualizations

### GPU Performance Across APIs

The chart below visualizes GPU performance across CUDA, OpenCL, and Vulkan APIs. This helps in identifying which GPUs excel in specific types of tasks and provides a comparative view of their capabilities.

<PlotlyLineChart
  data={{
    url: 'GPU_scores_graphicsAPIs.csv'
  }}
  title="GPU Performance Across APIs"
  xAxis="Device"
  yAxis="OpenCL"
/>

### NVIDIA GPU Price Forecast (2024 - 2029)

The bar chart below presents the projected prices of NVIDIA GPUs from 2024 to 2029, based on forecasts from Statista. This visualization provides insights into future price trends and helps in planning long-term investments.

<PlotlyLineChart
  data={{
    url: 'NVIDIA_PRICE.csv'
  }}
  title="Price Forecast of NVIDIA GPUs (2024-2029)"
  xAxis="year"
  yAxis="price"
/>

### NVIDIA Releases from 2013

This section provides an overview of key NVIDIA GPU releases starting from 2013.

<PlotlyLineChart
  data={{
    url: 'release_year_nvidia.csv'
  }}
  title="NVIDIA Releases from 2013"
  xAxis="release_year"
  yAxis="release"
/>

## Datasets used:

### GPU Benchmark

<FlatUiTable
  data={{
    url: 'GPU_benchmarks_v7.csv'
  }}
/>

### Nvidia Forecast

<FlatUiTable
  data={{
    url: 'NVIDIA_PRICE.csv'
  }}
/>

### Nvidia Release from 2013

<FlatUiTable
  data={{
    url: 'release_year_nvidia.csv'
  }}
/>

## Summary

- **Performance Metrics**: Provides a detailed view of GPU capabilities across various APIs, helping to identify which GPUs are best suited for specific applications and tasks.
- **Specifications**: Offers a comprehensive look at benchmarks, pricing, and power consumption, aiding in the selection of GPUs based on performance needs and budget considerations.
- **Visualizations**: The charts offer a clear perspective on GPU performance across different APIs and projected price trends, facilitating informed decision-making for current and future GPU investments.
