# AI ESG Digital Supply Chain Analysis

A statistical analysis toolkit examining whether artificial intelligence adoption improves Environmental, Social, and Governance performance through digital supply chain transformation. This repository contains mediation analysis code with bootstrap validation to test the pathway: AI Adoption → Digital Supply Chain Enhancement → ESG Performance.

## Overview

This project investigates the relationship between AI implementation and corporate sustainability outcomes. I developed this analysis to employ mediation techniques to determine whether AI influences ESG performance directly or through enhanced digital supply chain capabilities. I designed the toolkit to include bootstrap validation, moderation testing, and comprehensive visualisation capabilities.

## Features

I built this around classical mediation analysis using the Baron and Kenny framework, with bootstrap validation using 5,000 replications for robust inference. I included moderated mediation analysis with pre-calculated interaction terms, multiple regression models with control variables, and four-panel diagnostic visualisations. I made sure to add detailed business-focused interpretation of results.

To make the code output more visually appealing and engaging, I decided to try using icons and symbols throughout for the first time. This approach helps break up dense statistical text and makes it easier to spot key findings at a glance. The visual elements add some personality to what could otherwise be quite dry analytical output whilst keeping things professional.

## Requirements

### Core Dependencies
I kept the dependencies minimal:
```
pandas
numpy
matplotlib
seaborn
scipy
scikit-learn
```

## Installation

I made the installation straightforward:

1. Clone or download this repository
2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

## Data Setup

I designed the script to expect a CSV file with specific variables. Update the file path in the script:

```python
data = pd.read_csv("path/to/your/data.csv")
```

I built this to work with these required variables:
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

I designed this to run the complete analysis automatically:
```python
# The script executes automatically when run
# Results display in console with detailed interpretation
```

I structured the analysis to include:
- Data exploration and variable checking
- Three-step mediation pathway testing
- Bootstrap validation with confidence intervals
- Moderation effect testing
- Comprehensive result visualisation

### Individual Components

I organised the code so you can test specific mediation pathways:
```python
# Path A: AI → Digital Supply Chain
# Path B: Digital Supply Chain → ESG
# Indirect Effect: AI → Digital SC → ESG
```

I included functions to examine moderation effects:
```python
# Culture as moderator of AI effects
# Integration as moderator of Digital SC effects
```

I built diagnostic plot generation:
```python
# Scatterplots of key relationships
# Bootstrap distribution histogram
# Four-panel comprehensive visualisation
```

## Key Functions Reference

**Core Analysis:**
I wrote these key functions:
- `calculate_mediation_effect()` - Computes mediation coefficients for single sample
- Bootstrap loop - I designed this to repeat analysis 5,000 times for robust inference
- `calculate_ci()` - Generates confidence intervals from bootstrap results

**Visualisation:**
I created:
- Four-panel plot showing relationships and bootstrap distribution
- Scatter plots with trend lines for each pathway
- Histogram of indirect effects with confidence intervals

## Analysis Structure

I organised the analysis into five parts:

```
analysis/
├── Part 1: Basic Mediation Analysis    # Classical three-step testing
├── Part 2: Bootstrap Validation        # 5,000 replication inference
├── Part 3: Moderation Testing          # Conditional effects analysis
├── Part 4: Visualisation              # Diagnostic plots
└── Part 5: Interpretation             # Business-focused summary
```

## Statistical Output

I designed the analysis to provide:

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

I included these model assessment measures:

**Model Fit:**
- R-squared values for each regression equation
- Proportion of total effect explained by mediation

**Effect Sizes:**
- Standardised coefficients for interpretability
- Practical significance thresholds

## Result Interpretation

I built the interpretation around successful mediation evidence:
- Significant Path A (AI → Digital SC)
- Significant Path B (Digital SC → ESG)
- Significant indirect effect with confidence interval excluding zero
- Meaningful proportion of total effect mediated

**Bootstrap Validation:**
I designed the bootstrap validation to provide:
- Confidence intervals for robust statistical inference
- Distribution shape to indicate assumption validity
- Replication consistency to demonstrate result reliability

## Configuration Options

I made the key parameters adjustable:

```python
# Bootstrap replications
n_bootstrap = 5000

# Confidence level
confidence = 0.95

# Control variables
controls = ['Firm_Size', 'ROA', 'Leverage']
```

## Troubleshooting

**Missing variables:** I built this to be particular about variable names - check column names match script expectations exactly. Case sensitivity matters for variable identification.

**Sample size issues:** I designed the bootstrap methods for adequate sample sizes. Very small datasets may produce unstable results.

**Convergence problems:** I've found that extreme outliers or multicollinearity can affect regression stability. Examine data quality before analysis.

**Interpretation difficulties:** I included detailed console output that provides step-by-step explanations of each analysis component.

## Limitations

I'm aware of these limitations in the current implementation:
- Cross-sectional data limits causal inference capabilities
- Linear relationship assumptions may not capture complex interactions
- Unmeasured confounders could bias mediation estimates
- Industry and temporal effects not explicitly modelled in basic specification

## Theoretical Framework

I designed this analysis to test the proposition that AI adoption improves ESG performance primarily through enhanced digital supply chain capabilities rather than direct effects. This mediation hypothesis suggests organisations should focus AI investments on supply chain applications to maximise sustainability benefits.

## Expected Applications

I built this with two main applications in mind:

**Academic Research:**
- Template for organisational mediation studies
- Bootstrap methodology for robust statistical inference
- Moderation testing with interaction terms

**Business Practice:**
- Evidence-based AI investment prioritisation
- Understanding mechanisms linking technology and sustainability
- Identifying contextual factors affecting AI effectiveness

## Data Sources

I designed this to be compatible with corporate datasets containing:
- Technology adoption measures
- Supply chain digitalisation indices
- ESG performance scores
- Standard financial and organisational control variables
  Reference: World Bank. (2023). [World Development Indicators: Population (Version 1)](https://doi.org/10.7910/DVN/UEBOES). Harvard Dataverse.

## Contributing

I'd welcome contributions in these areas for enhancement:
- Longitudinal analysis capabilities
- Industry-specific moderation effects
- Non-linear mediation pathways
- Additional control variable specifications
- Sensitivity analysis features

## License

MIT License - see LICENSE file for details.

## Acknowledgments

I built this using standard Python data science libraries. The methodology follows established practices in organisational research and statistical mediation analysis.
