# Task 08 — Detecting Bias in LLM-Generated Data Narratives

This repository contains the **experimental design and scaffolding** for Task 08 (Controlled Experiment on LLM Bias).  
The goal is to determine whether identical datasets yield different narratives depending on how questions are framed.

## Setup
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## Run Workflow
1. Generate or review prompts in `prompts/prompt_templates.json`  
2. Run dry experiments:  
   ```bash
   python scripts/run_experiment.py --prompts prompts/prompt_templates.json --out results/raw
   ```  
3. Analyze when responses available:  
   ```bash
   python scripts/analyze_bias.py --in results/raw --out analysis
   ```

## Repo Notes
- **No datasets** are committed. All identifiers are anonymized.  
- `.gitignore` excludes all data and intermediate results.  
- Model outputs will be collected later for the Nov 15 report.