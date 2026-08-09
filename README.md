# COVID-19 International Spread Chain Analysis 🌍

This project presents an interpretable data mining framework for reconstructing the international spread chain of COVID-19 using association rule mining, network analysis on country-level first-case travel-origin data.

## Overview

Country-level first-case records are processed at the country level and analyzed using directed network construction, association rule mining, and sequential pattern mining to extract travel-origin and transmission-related patterns. A binary origin-destination matrix is used to fairly compare pattern-mining algorithms, while a richer feature-engineered dataset supports deeper association rule discovery. Multiple analytical methods are evaluated to identify dominant travel-origin countries, temporal and structural spread patterns, and the most interpretable pattern-mining approach.

## Dataset

* Covid-19 world-wide Dataset or Dataset A (186 countries)
* Dataset A — 186 rows × 8 fields (continent, first-case date, travel origin, etc.)
* Dataset B — 215 rows × 22 engineered features (multi-origin countries exploded into rows)
* Binary Spread-Chain Matrix — 42 source countries × 186 destination countries
* Directed Origin-Destination Network — 178 nodes, 202 edges

## Methods

Directed Network Analysis, Association Rule Mining (Apriori), Frequent Pattern Growth (FP-Growth), Sequential Pattern Mining (PrefixSpan), Temporal Analysis, and Community Detection.

The experiments identified Italy as the top country by direct reach (out-degree) and China as the top country by betweenness centrality, with Apriori and FP-Growth producing identical frequent itemsets and rules on matched data.

## Explainability

Model outputs are interpreted using:

* Degree, Betweenness, Closeness, and PageRank Centrality
* Greedy Modularity Community Detection
* Support, Confidence, and Lift Thresholds for Rule Strength
* Centrality Correlation Analysis
* Statistical Validation (Permutation Test, Chi-Square Test, Fisher's Exact Test)

## Output

The framework provides:

* Ranked Travel-Origin Countries by Reach and Bridge Centrality
* Temporal and Geographic Spread Patterns
* Association Rules with Support / Confidence / Lift
* Multi-Hop Transmission Path and Community Structure
* Comparative Runtime and Rule-Count Evaluation Across Algorithms

## Technologies

Python • NetworkX • mlxtend • Pandas • Matplotlib • SciPy • Apriori • FP-Growth • PrefixSpan
