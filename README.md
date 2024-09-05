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
    description: This dataset contains over 300 listed GPU / video cards / graphics cards with specs and the latest prices that were all scraped in the web database Pcbuilder. Unfortunately, only items that had price displays were included. United States was the selected location, so expect the prices in United States Dollars USD currency.
    lastModified: 2024-09-03
    path: gpu_specs_prices.csv
---
# GPU Dataset Analysis

## Overview

This dataset provides a comprehensive view of various GPUs, including performance metrics across different APIs and detailed specifications. The analysis helps in comparing GPU performance and evaluating their value based on benchmarks and pricing.

## Data Sections

### 1. GPU Performance Metrics

This section includes performance metrics for GPUs across CUDA, Metal, OpenCL, and Vulkan APIs.

<FlatUiTable
  data={{
    url: 'GPU_scores_graphicsAPIs.csv'
  }}
/>

#### Key Insights

- **CUDA Performance**: The top-performing GPUs in CUDA are the GeForce RTX 3090 Ti and A100 series, showing exceptional computational power.
- **API Versatility**: NVIDIA GPUs, such as the RTX 3090 and 3080 series, demonstrate strong performance across OpenCL and Vulkan, indicating their robustness in various tasks.

### 2. GPU Specifications

This section covers GPU benchmark scores, pricing, power consumption (TDP), and other specifications.

<FlatUiTable
  data={{
    url: 'GPU_benchmarks_v7.csv'
  }}
/>

#### Key Insights

- **Benchmark Scores**: The GeForce RTX 3090 Ti achieves the highest G3Dmark score, indicating superior graphical performance. The RTX 3080 Ti and RTX 3090 also deliver high performance.
- **Pricing and Value**: High-end GPUs like the RTX A6000 and Titan RTX are more expensive, while GPUs such as the RTX 3070 offer strong performance at a lower cost.
- **Power Consumption**: GPUs with higher TDP ratings, such as the RTX 3090 Ti, require more power, which is a key consideration for system integration.

## Data Visualizations

### GPU Performance Across APIs

The following chart illustrates the performance of GPUs across CUDA, OpenCL, and Vulkan APIs. This visualization helps to identify which GPUs excel in specific types of tasks.

<PlotlyLineChart
  data={{
    url: 'GPU_scores_graphicsAPIs.csv'
  }}
  title="GPU Performance Across APIs"
  xAxis="Device"
  yAxis="CUDA"
/>

### Benchmark Scores vs. Pricing

The chart below compares GPU benchmark scores with pricing. This visualization highlights the cost-effectiveness of various GPUs by comparing their G3Dmark scores, which reflect graphical performance, against their prices. It provides insights into how pricing relates to performance, helping to evaluate the value of each GPU.

<PlotlyLineChart
  data={{
    url: 'GPU_benchmarks_v7.csv'
  }}
  title="Benchmark Scores vs. Pricing"
  xAxis="gpuName"
  yAxis="G3Dmark"
/>

### NVIDIA GPU Price forecast (2024 - 2029)

<PlotlyLineChart
  data={{
    url: 'NVIDIA_PRICE.csv'
  }}
  title="Forecast of NVIDIA Price in US 2024-2029"
  xAxis="year"
  yAxis="price"
/>


## Summary

- **Performance Metrics**: Provides insight into GPU capabilities across different APIs, showing which GPUs are best suited for specific applications.
- **Specifications**: Offers a detailed look at benchmarks, pricing, and power consumption, aiding in the selection of GPUs based on performance and budget.
- **Visualizations**: The charts offer a clear view of performance across APIs and the relationship between benchmark scores and pricing, facilitating better decision-making.

Feel free to explore the provided tables and charts for a deeper understanding of GPU performance and value.

