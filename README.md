
# Pricing Optimization Challenge - Solution Summary

## Solution Overview

This project implements a comprehensive pricing optimization solution using price elasticity modeling and dynamic pricing simulation. The solution analyzes historical sales data to determine optimal pricing strategies that maximize profit while considering demand sensitivity.

### Key Components

1. **Data Integration & Cleaning**: Combines multiple sales datasets with standardized schemas
2. **Price Elasticity Modeling**: Uses log-log regression to calculate demand elasticity by product category
3. **Dynamic Pricing Simulation**: Applies economic optimization formulas to determine profit-maximizing prices
4. **Performance Evaluation**: Quantifies potential profit improvements from pricing changes

### Methodology

- **Elasticity Calculation**: Log-log regression model where elasticity coefficient represents percentage change in quantity for 1% price change
- **Optimization Formula**: For elastic products (elasticity < -1): `optimal_price = cost × (elasticity / (1 + elasticity))`
- **Profit Simulation**: Compares baseline vs. optimized scenarios using elasticity-adjusted demand forecasts

## Setup Instructions

### Prerequisites
- Python 3.8+
- uv package manager

### Environment Setup

1. **Clone the repository:**
```bash
git clone <repository-url>
cd data-science-assignment
```

2. **Sync dependencies with uv:**
```bash
uv sync
```

3. **Verify installation:**
```bash
uv run python -c "import polars, numpy, statsmodels, matplotlib, seaborn; print('All packages installed successfully')"
```

### Data Requirements

Ensure the following CSV files in the project ./data directory:
- `Amazon Sale Report.csv` - Primary transactional data
- `International sale Report.csv` - Additional sales with pricing data
- `P&L March 2021.csv` - Cost data for profit calculations

## How to Run

### Jupyter Notebook

1. **Start Jupyter with uv environment:**
```bash
uv run jupyter notebook
```

2. **Open the analysis notebook:**
    - Navigate to and open `pricing_optimization_analysis.ipynb`
    - **Important**: Select the uv environment as your kernel
    - Go to `Kernel` → `Change kernel` → Select the uv environment
    - Verify the correct environment is active in the top-right corner

3. **Run the step-by-step analysis:**
    - Methodology Overview
    - 1. Environment Setup and Library Imports
    - 2. Data Loading and Initial Inspection
    - 3. Data Aggregation for Modeling
    - 4. Categorize Segments for Action
    - 5. Calculate the Baseline vs. Simulated Profits

### Expected Outputs

- Elasticity coefficients by product category
- Visualization of demand sensitivity
- Profit improvement projections
- Category-wise optimization recommendations

### Key Results
Refer to `results/analysis.xlsx` and `results/Output Document.docx` for summary of the results.

## AI Assistance

The following AI tools were used to assist in developing this solution:

- GitHub Copilot Chat - for code boilerplate, generating readme and EDA
- GitHub Copilot Autocomplete - for generating code as per inline comments
