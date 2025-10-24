# Sim Loyalty

A powerful, interactive customer retention and growth simulator that helps you model and predict customer base dynamics over time.

## Overview

Sim Loyalty uses a **three-segment retention model** to simulate how customer cohorts behave over time. By dividing customers into short-term, medium-term, and long-term retention segments, you can:

- 📊 Model realistic customer retention curves
- 📈 Predict long-term customer base growth
- 🎯 Calculate key metrics like median lifetime, mean lifetime, and growth asymptotes
- 🔧 Fit theoretical models to your actual retention data

## Features

### Three-Segment Retention Model
Divide your customer base into segments based on longevity:
- **Short-term**: High churn, typically exploratory users
- **Medium-term**: Moderate retention, regular users
- **Long-term**: Low churn, highly engaged customers

### Interactive Visualizations
- **Single Cohort Retention**: See how one cohort decays over time
- **Multi-Cohort Growth**: Model total customer base with monthly acquisition
- Real-time chart updates as you adjust parameters

### Curve Fitting
Upload your actual retention data and automatically fit the three-segment model to match your observed patterns. Perfect for working with real cohort data from your analytics platform.

### Key Metrics
- **Median Customer Lifetime**: When 50% of customers have churned
- **Mean Customer Lifetime**: Average customer lifespan
- **Growth Asymptote**: Steady-state customer base (if churn > 0)

## Getting Started

### Live Demo
Visit the hosted version at: **https://roenbaeck.github.io/sim-loyalty/**

### Local Usage
Simply open `index.html` in your web browser. No installation or build process required!

### Basic Usage

1. **Set Monthly Acquisition**: How many new customers you acquire each month
2. **Define Retention Segments**: 
   - Set the percentage split (must sum to 100%)
   - Set monthly churn rate for each segment
3. **Run Simulation**: Adjust duration and click "Update Charts"

### Advanced: Fit to Real Data

1. Click "🎯 Fit Model to Data" 
2. Paste your retention percentages (one per month, starting at 100%)
3. Click "Run Fit" to automatically calculate optimal segment parameters
4. Review the fitted values and adjust manually if needed

## Use Cases

- **SaaS/Subscription Planning**: Model MRR growth and churn scenarios
- **E-commerce Retention**: Predict repeat purchase patterns
- **Mobile Apps**: Understand user engagement and lifecycle
- **Marketplaces**: Balance supply/demand growth with retention
- **Product Strategy**: Evaluate impact of retention improvements

## Technical Details

### Model Assumptions
- Monthly time periods (suitable for most businesses)
- Exponential decay within each segment
- Constant monthly churn rates per segment
- Fixed monthly customer acquisition

### Calculations
- Retention uses compound decay: `remaining(t) = initial × (1 - churn_rate)^t`
- Growth sums all active cohorts at each time point
- Asymptote (if exists): `sum(segment_size / segment_churn_rate)` for each segment

## Tips

- **Start with default values** to understand model behavior
- **Use real data**: The curve fitting feature works best with 6-12+ months of data
- **Validate assumptions**: Compare model output with your actual metrics
- **Iterate**: Adjust segment percentages to better match observed patterns
- **Experiment**: Test "what-if" scenarios by varying acquisition or churn rates

## License

See [LICENSE](LICENSE) file for details.

## Deployment

This project uses GitHub Pages for hosting:

1. Go to **Settings** → **Pages** in your GitHub repository
2. Under "Source", select **main** branch
3. Save and wait a few minutes for deployment
4. Access at `https://roenbaeck.github.io/sim-loyalty/`

Changes pushed to the main branch are automatically deployed.

## Contributing

This is a single-file HTML application. Feel free to fork, modify, and improve!

