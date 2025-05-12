# Earthquake Analysis Web App

<div align="center">
  <img src="banner.png" alt="Earthquake Dashboard Banner" width="100%">
</div>

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-blue.svg" alt="Python 3.9+">
  <img src="https://img.shields.io/badge/Streamlit-1.20+-00BFFF.svg" alt="Streamlit 1.20+">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="MIT License">
</div>

<div align="center">
  <p>
    <b>Interactive visualization and analysis of global seismic activity data</b>
  </p>
  <p>
    <i>Powered by Streamlit, Plotly, Pandas, and Scikit-learn</i>
  </p>
  <p>
    <a href="../earthquakes"><b>📊 View the companion Data Analysis Project</b></a>
  </p>
</div>

## 📋 Overview

Provides an interactive interface for exploring and analyzing seismic data from the USGS Earthquake Catalog. The application allows users to visualize earthquake patterns, perform spatial clustering, and identify temporal trends in seismic activity.

> **🔍 Data Science Foundation:** This application builds upon the analytical work in our [Earthquake Data Analysis](https://github.com/anverpy/earthquakes) project, which provides the data processing pipeline, statistical analysis, and visualization techniques that power this dashboard.

### 🌟 Key Features

- **Interactive Data Filtering:** Filter earthquakes by date, magnitude, depth, event type, and geographic region
- **Comprehensive Visualizations:** Explore data through histograms, scatter plots, maps, and heatmaps
- **Geographic Analysis:** Visualize the spatial distribution of earthquakes with interactive maps
- **Clustering Analysis:** Apply DBSCAN algorithm to identify geographic clusters of seismic events
- **Temporal Pattern Detection:** Analyze daily, weekly, and hourly patterns of earthquake activity
- **Advanced Analytics:** Examine correlations between variables and compare earthquake characteristics across regions

## 🛠️ Technology Stack

- **Streamlit:** Interactive web application framework
- **Pandas & NumPy:** Data manipulation and numerical computations
- **Plotly Express:** Interactive data visualizations
- **Scikit-learn:** Machine learning for clustering analysis (DBSCAN)
- **Matplotlib:** Additional visualization capabilities

## 🚀 Getting Started

### Prerequisites

- Python 3.9 or higher
- pip package manager

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/earthquakes-app.git
   cd earthquakes-app
   ```

2. Create and activate a virtual environment (recommended):
   ```bash
   python -m venv earthquakesenv
   source earthquakesenv/bin/activate  # On Windows: earthquakesenv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Download the latest earthquake data:
   ```bash
   # Option 1: Use processed data from the Earthquake Data Analysis project
   cp ../earthquakes/cleaned_dataframe.csv data/earthquakes.csv
   
   # Option 2: Data will be automatically downloaded if not present
   # Or manually download from https://earthquake.usgs.gov/earthquakes/feed/v1.0/csv.php
   # and place in /data
   ```

5. Run the application:
   ```bash
   streamlit run app.py
   ```

## 📊 Dashboard Structure

The dashboard is organized into four main sections:

### 1. General Summary
- Overview metrics of the selected earthquake data
- Distribution visualizations for magnitude and depth
- Relationship analysis between magnitude and depth
- Top regions with highest seismic activity

### 2. Geographic Analysis
- Interactive global map of earthquake events
- Heat map showing areas with concentrated seismic activity
- Cluster analysis using DBSCAN algorithm to identify related event groups

### 3. Temporal Analysis
- Daily evolution of seismic activity
- Weekly patterns visualization
- Hourly distribution analysis with heat maps

### 4. Advanced Analysis
- Correlation matrix between earthquake parameters
- Magnitude analysis by region
- Comparative studies of different parameters

## 📷 Screenshots

*[Screenshots would be added here]*

## 🧪 Data Processing

The application processes earthquake data through several steps:

```
Raw USGS Data → Data Loading → Preprocessing → Filtering → Analysis → Visualization
```

Key processing steps include:
- Time zone standardization
- Category assignment based on magnitude
- Data filtering based on user inputs
- Statistical aggregation for trend analysis
- Geographic and temporal pattern detection

## 🔍 Advanced Features

### DBSCAN Clustering

The application implements the Density-Based Spatial Clustering of Applications with Noise (DBSCAN) algorithm to identify clusters of earthquakes that may be related. This helps in:

- Identifying aftershock sequences
- Detecting swarm activity
- Visualizing spatial patterns of seismic events

Users can adjust clustering parameters:
- `eps`: Maximum distance between points to be considered neighbors
- `min_samples`: Minimum number of points required to form a cluster

### Temporal Pattern Analysis

The dashboard offers tools to detect patterns in earthquake occurrence over time:
- Daily trends and magnitude evolution
- Day-of-week distribution
- Hour-of-day patterns
- Interactive heat maps for temporal-spatial correlations

## 🔗 Related Projects

This application is part of a comprehensive earthquake analysis suite:

### [📊 Earthquake Data Analysis](https://github.com/anverpy/earthquakes)

<p align="center">
  <img src="../earthquakes/Graphics/earthquake_heatmap.png" alt="Earthquake Data Analysis" width="600"/>
</p>

The Earthquake Data Analysis project provides:

- **Advanced data preprocessing** techniques used in this dashboard
- **Statistical analysis** and insights that inform the visualizations
- **Jupyter notebooks** showing the step-by-step analytical process
- **Correlation studies** that help explain relationships in seismic data

This dashboard brings the insights from the analysis project to life through an interactive interface.


## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- USGS for providing open access to earthquake data
- The Streamlit team for their excellent framework
- Contributors to the Python data science ecosystem

---

<div align="center">
  <p>Developed for educational and research purposes</p>
  <p>© 2025 Your Name</p>
</div>
