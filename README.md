# Time Series Analysis of Climate Change Data

## Overview
This analysis examines historical temperature anomaly data from 1850 to 2022, applying time series forecasting techniques to project future climate trends through 2050. The study evaluates warming patterns and their potential environmental impacts.

## Summary of Results

### Primary Conclusions
- Temperature anomalies demonstrate a consistent upward trajectory, with particularly rapid increases in recent decades
- Model projections suggest temperature anomalies will rise by approximately 1.5°C by 2050
- The ARIMA(1,1,3) model incorporating drift produced optimal forecasting performance
- Bootstrap validation using ETS models reinforces the statistical robustness of observed trends

### Technical Methodology

#### Data Processing Phase
- Analysis utilizes historical climate anomaly records spanning 1850-2022
- Box-Cox transformation assessment indicated optimal lambda parameter of 1.23
- Stationarity was achieved through first-order differencing, validated by unit root diagnostics

#### Modeling Framework
- Multiple ARIMA specifications were evaluated, both with and without drift components
- Model selection criteria included AIC, AICc, and BIC metrics
- ARIMA(1,1,3) with drift demonstrated superior performance across evaluation metrics

#### Analytical Enhancements
- STL decomposition isolated trend, seasonal, and residual components
- Block bootstrapping with 100 replications (block size = 8) assessed model stability
- Ensemble techniques aggregated predictions from bootstrapped ETS models

#### Model Verification
- ACF and PACF analysis examined autocorrelation patterns in differenced series
- Residual diagnostics validated model assumptions
- Comparative evaluation of multiple model specifications ensured robustness

## Implementation Details

### Computational Environment
- Primary analysis conducted in R utilizing the fpp3 framework (tsibble, fable, feasts packages)
- Supporting packages included tidyverse, lubridate, readxl, and ggplot2
- Methodological approaches incorporated ARIMA specification, STL decomposition, bootstrap resampling, and ETS forecasting

### Interpretive Analysis

#### Historical Temperature Patterns
- 1850-1900: Period characterized by relative stability with minimal variation
- 1900-1980: Moderate but consistent increase in temperature anomalies
- 1980-2022: Marked acceleration in warming trend
- Peak anomaly recorded in 2022 at +1.03°C

#### Projection Confidence Intervals
- Near-term forecasts (2023-2035) exhibit higher confidence with narrower prediction bands
- Long-term projections (2036-2050) show wider uncertainty intervals
- Important caveat: Future policy interventions and environmental measures may substantially alter forecast trajectories
