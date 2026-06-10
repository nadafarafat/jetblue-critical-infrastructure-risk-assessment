# JetBlue Airways Critical Infrastructure Risk Assessment

**A Model-Based Risk Assessment of JetBlue's Domestic Route Network**

[![Course](https://img.shields.io/badge/Course-Security%20Risk%20Management-blue)]()
[![Framework](https://img.shields.io/badge/Framework-MBRA-green)]()
[![Network](https://img.shields.io/badge/Nodes-14-orange)]()

## Overview

Comprehensive cybersecurity risk analysis of JetBlue Airways' 14-node domestic route network using complex network analysis, Mission-Based Risk Assessment (MBRA), and Fault Tree Analysis (FTA). Developed policy recommendations for the Department of Homeland Security.

**Course:** CY 7790 - Security Risk Management & Decision Making for Critical Infrastructure  
**Professor:** Themis Papageorge (PhD MIT, Former VP at Guardium)  
**Institution:** Northeastern University  
**Author:** Mohammed Arafat Nadaf

## Key Findings

| Metric | Value |
|--------|-------|
| Total Network Risk Exposure | $114.3M |
| Blocking Nodes (JFK + BOS) | 51% of total risk ($58.3M) |
| Critical Vulnerability Threshold (γ₀) | 20.45% |
| Spectral Radius (ρ) | 7.542 |
| Recommended Annual Budget | $71.06M |
| Projected Risk Reduction | 75% |

## Methodology

### Network Analysis
- Modeled JetBlue's 14-node network as undirected cascade network
- Calculated adjacency matrix and spectral properties
- Identified blocking nodes using degree and betweenness centrality
- Derived resilience equation: q = 10^(0.2051 - 1.0031γ)

### MBRA (Mission-Based Risk Assessment)
- Threat probability estimation per node (0.40 - 0.95)
- Vulnerability assessment based on historical incidents
- Consequence modeling using Delta CrowdStrike benchmark ($550M)
- Prevention and response budget optimization

### Fault Tree Analysis
- JFK Node: 3 attack paths (External, Insider, Third-Party)
- BOS Node: 3 attack paths (Direct, Cascade from JFK, Supply Chain)
- Calculated top event probabilities and elimination costs

## Network Nodes

| Rank | Node | City | Risk ($M) | Classification |
|------|------|------|-----------|----------------|
| 1 | JFK | New York | 34.9 | Critical - Blocking Node |
| 2 | BOS | Boston | 23.4 | Critical - Blocking Node |
| 3 | LAX | Los Angeles | 12.1 | High - West Coast Bridge |
| 4 | FLL | Fort Lauderdale | 10.7 | High - Florida Hub |
| 5 | MCO | Orlando | 7.7 | Medium |
| 6 | SJU | San Juan | 6.9 | Medium |
| 7-14 | Others | Various | 0.7-5.0 | Low |

## Attack Vector Analysis

### Cyber Attack Vectors
- Phishing campaigns (P = 0.60)
- Ransomware via vendor systems (P = 0.50)
- API exploitation in booking systems (P = 0.60)
- Insider threats (P = 0.40)

### Targeted Attack Impact
- BOS compromise: 13 routes affected, 18,000 passengers stranded, $40M loss
- JFK compromise: 12 routes affected, 25,000 passengers stranded, $52.5M loss
- Combined attack: 85% network isolation, $100M+ losses

## ROI Analysis

| Scenario | Investment | Risk Reduction | ROI |
|----------|------------|----------------|-----|
| Blocking nodes only | $9.9M | 51% | 5.89:1 |
| Critical + High priority | $23.2M | 65% | 3.50:1 |
| Full network | $71.06M | 75% | 1.21:1 |

Response investments (3.34:1 ROI) outperform prevention investments (1.79:1 ROI).

## DHS Policy Recommendations

1. Designate JFK and BOS as Critical Aviation Cyber Infrastructure
2. Mandate cascade risk assessment for major airline networks
3. Establish inter-airline threat intelligence sharing protocols
4. Create Aviation Cyber Reserve Fund for rapid response
5. Require network segmentation standards
6. Develop joint DHS/TSA/airline SOC capabilities

## Tools & Techniques

- Python (NetworkX, NumPy) for network analysis
- MBRA Tool for risk quantification
- Fault Tree Analysis for attack path modeling
- Spectral analysis for cascade susceptibility
- Eigenvector centrality calculations

## References

- Eurocontrol (2024) - Aviation Cybersecurity Annual Report
- IBM X-Force (2024) - Transportation Sector Threat Intelligence
- Delta Air Lines CrowdStrike Incident (2024) - $550M benchmark
- NIST Cybersecurity Framework 2.0
- CISA Transportation Systems Sector Guidelines

## Disclaimer

This research was conducted for academic purposes under the Security Risk Management course at Northeastern University. All analysis is based on publicly available information and theoretical modeling.

---

**Author:** Mohammed Arafat Nadaf  
**GitHub:** github.com/nadafarafat  
**LinkedIn:** linkedin.com/in/arafatnadaf
