# AI ESG Digital Supply Chain Analysis

A statistical analysis toolkit examining whether artificial intelligence adoption improves Environmental, Social, and Governance performance through digital supply chain transformation. This repository contains mediation analysis code with bootstrap validation to test the pathway: AI Adoption → Digital Supply Chain Enhancement → ESG Performance.

## Overview

This project investigates the relationship between AI implementation and corporate sustainability outcomes. The analysis employs mediation techniques to determine whether AI influences ESG performance directly or through enhanced digital supply chain capabilities. The toolkit includes bootstrap validation, moderation testing, and comprehensive visualisation capabilities.

## Features

- Classical mediation analysis using Baron and Kenny framework
- Bootstrap validation with 5,000 replications for robust inference
- Moderated mediation analysis with pre-calculated interaction terms
- Multiple regression models with control variables
- Four-panel diagnostic visualisations
- Detailed business-focused interpretation of results

## Requirements

### Core Dependencies
```
pandas
numpy
matplotlib
seaborn
scipy
scikit-learn
```

## Installation

1. Clone or download this repository
2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

## Data Setup

The script expects a CSV file with specific variables. Update the file path in the script:

```python
data = pd.read_csv("path/to/your/data.csv")
```

Required variables:
- AI_Adoption: Measure of artificial intelligence implementation
- Digital_SC_Transformation: Digital supply chain capabilities index
- ESG_Score: Environmental, social, governance performance measure
- Firm_Size: Company size control variable
- ROA: Return on assets control variable
- Leverage: Financial leverage control variable
- Culture_Index: Organisational culture measure
- Integration_Index: Systems integration capability
- AIxCulture: Pre-calculated AI × Culture interaction
- DSCxIntegration: Pre-calculated Digital SC × Integration interaction

## Usage

### Basic Analysis

Run the complete analysis:
```python
# The script executes automatically when run
# Results display in console with detailed interpretation
```

The analysis includes:
- Data exploration and variable checking
- Three-step mediation pathway testing
- Bootstrap validation with confidence intervals
- Moderation effect testing
- Comprehensive result visualisation

### Individual Components

Test specific mediation pathways:
```python
# Path A: AI → Digital Supply Chain
# Path B: Digital Supply Chain → ESG
# Indirect Effect: AI → Digital SC → ESG
```

Examine moderation effects:
```python
# Culture as moderator of AI effects
# Integration as moderator of Digital SC effects
```

Generate diagnostic plots:
```python
# Scatterplots of key relationships
# Bootstrap distribution histogram
# Four-panel comprehensive visualisation
```

## Key Functions Reference

**Core Analysis:**
- `calculate_mediation_effect()` - Computes mediation coefficients for single sample
- Bootstrap loop - Repeats analysis 5,000 times for robust inference
- `calculate_ci()` - Generates confidence intervals from bootstrap results

**Visualisation:**
- Four-panel plot showing relationships and bootstrap distribution
- Scatter plots with trend lines for each pathway
- Histogram of indirect effects with confidence intervals

## Analysis Structure

```
analysis/
├── Part 1: Basic Mediation Analysis    # Classical three-step testing
├── Part 2: Bootstrap Validation        # 5,000 replication inference
├── Part 3: Moderation Testing          # Conditional effects analysis
├── Part 4: Visualisation              # Diagnostic plots
└── Part 5: Interpretation             # Business-focused summary
```

## Statistical Output

The analysis provides:

**Path Coefficients:**
- Path A: Effect of AI on Digital Supply Chain transformation
- Path B: Effect of Digital Supply Chain on ESG performance
- Direct Effect: Remaining AI influence on ESG when mediator included
- Indirect Effect: AI influence transmitted through Digital Supply Chain

**Bootstrap Results:**
- Mean effects across 5,000 samples
- 95% confidence intervals for each pathway
- Statistical significance testing based on zero exclusion

**Moderation Analysis:**
- Main effects and interaction coefficients
- Assessment of conditional mediation pathways

## Performance Metrics

**Model Fit:**
- R-squared values for each regression equation
- Proportion of total effect explained by mediation

**Effect Sizes:**
- Standardised coefficients for interpretability
- Practical significance thresholds

## Result Interpretation

**Successful Mediation Evidence:**
- Significant Path A (AI → Digital SC)
- Significant Path B (Digital SC → ESG)
- Significant indirect effect with confidence interval excluding zero
- Meaningful proportion of total effect mediated

**Bootstrap Validation:**
- Confidence intervals provide robust statistical inference
- Distribution shape indicates assumption validity
- Replication consistency demonstrates result reliability

## Configuration Options

Adjust analysis parameters:

```python
# Bootstrap replications
n_bootstrap = 5000

# Confidence level
confidence = 0.95

# Control variables
controls = ['Firm_Size', 'ROA', 'Leverage']
```

## Troubleshooting

**Missing variables:** Check column names match script expectations exactly. Case sensitivity matters for variable identification.

**Sample size issues:** Bootstrap methods require adequate sample sizes. Very small datasets may produce unstable results.

**Convergence problems:** Extreme outliers or multicollinearity can affect regression stability. Examine data quality before analysis.

**Interpretation difficulties:** Review the detailed console output which provides step-by-step explanations of each analysis component.

## Limitations

- Cross-sectional data limits causal inference capabilities
- Linear relationship assumptions may not capture complex interactions
- Unmeasured confounders could bias mediation estimates
- Industry and temporal effects not explicitly modelled in basic specification

## Theoretical Framework

The analysis tests the proposition that AI adoption improves ESG performance primarily through enhanced digital supply chain capabilities rather than direct effects. This mediation hypothesis suggests organisations should focus AI investments on supply chain applications to maximise sustainability benefits.

## Expected Applications

**Academic Research:**
- Template for organisational mediation studies
- Bootstrap methodology for robust statistical inference
- Moderation testing with interaction terms

**Business Practice:**
- Evidence-based AI investment prioritisation
- Understanding mechanisms linking technology and sustainability
- Identifying contextual factors affecting AI effectiveness

## Data Sources

Compatible with corporate datasets containing:
- Technology adoption measures
- Supply chain digitalisation indices
- ESG performance scores
- Standard financial and organisational control variables
- World Bank. (2023). [World Development Indicators: Population (Version 1)](https://doi.org/10.7910/DVN/UEBOES). Harvard Dataverse.

## Contributing

Areas for enhancement include:
- Longitudinal analysis capabilities
- Industry-specific moderation effects
- Non-linear mediation pathways
- Additional control variable specifications
- Sensitivity analysis features

## License

MIT License - see LICENSE file for details.

## Acknowledgments

Built using standard Python data science libraries. The methodology follows established practices in organisational research and statistical mediation analysis.
