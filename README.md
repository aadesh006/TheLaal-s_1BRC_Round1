# TechNex'25: 1 Billion Row Challenge (Round 1)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![Pandas](https://img.shields.io/badge/Library-Pandas-150458) ![Status](https://img.shields.io/badge/Status-Completed-success)

This repository contains the solution code for **Round 1** of the **1 Billion Row Challenge** hosted during **TechNex 2025 at IIT BHU**. The solution focuses on efficient data ingestion, duplicate handling, statistical analysis, and visualization of sensor data.

---

## Project Overview

The objective of this challenge was to process a large dataset (`sensor_data.csv`), perform data cleaning, compute statistical metrics, and visualize the results while monitoring system resources (CPU and execution time).

### Key Features
* **Performance Monitoring:** Tracks execution time and CPU usage before and after processing using `psutil`.
* **Data Ingestion:** Loads CSV data into a Pandas DataFrame.
* **Data Cleaning:** Identifies and removes duplicate rows to ensure data integrity.
* **Feature Engineering:** Creates a derived column `combined_value` (Sensor Reading + Control Value).
* **Statistical Analysis:** Computes Mean, Median, and Mode for key data columns.
* **Visualization:** Generates a grouped bar chart comparing statistical metrics across columns.

---

## Dependencies

To run this code, you need Python installed along with the following libraries:

* `pandas` (Data manipulation)
* `numpy` (Numerical operations)
* `matplotlib` (Visualization)
* `psutil` (System monitoring)

You can install the dependencies using pip:

```bash
pip install pandas numpy matplotlib psutil
```

---

### Methodology

* The script follows a linear processing pipeline:
* Initialization: Records start time and initial CPU usage.
* Ingestion: Reads the raw CSV file.
* Duplicate Removal: Checks for and drops duplicate entries.
* Processing:
  Calculates combined_value = sensor_reading + control_value.
  Helper function compute_stats() extracts Mean, Median, and Mode.
* Visualization: Plots a comparative bar chart using Matplotlib.
* Benchmarking: Outputs total runtime and CPU overhead.
