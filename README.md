Psychology + Machine Learning Experiments
Originally created for exploring probabilistic reinforcement learning (PRL) datasets,
this repository now focuses on behavioural modelling of the Attention Network Task (ANT) using open neuro data from OpenNeuro ds001907.
The goal is to develop and test machine learning pipelines for analysing human behavioural data, starting with attention and reaction-time paradigms and later extending to learning and decision-making tasks.

🧠 Overview
This project demonstrates how to:
Load and process open-access psychology/neuroscience datasets (e.g., from OpenNeuro)
Extract and engineer features from trial-by-trial event data (.tsv files)
Analyse patterns in reaction time, accuracy, and attentional control
Train and evaluate ML models to predict cognitive performance
Build reproducible workflows (data → analysis → visualisation)

📂 Folder Structure
data/
│
├── raw/                # Unmodified datasets (ignored in git)
│   └── ds001907/       # ANT dataset from OpenNeuro
├── interim/            # Cleaned / filtered data
├── processed/          # Model-ready datasets
│
notebooks/              # Jupyter notebooks for exploration & modelling
src/                    # Python scripts (data loading, preprocessing, modelling)
reports/                # Figures, tables, and notes
papers/                 # Reference literature and reading notes

🧩 Current Focus
Dataset
Attention Network Task (ANT) — a cognitive paradigm measuring:
Alerting – maintaining readiness to respond
Orienting – shifting attention to spatial cues
Executive control – resolving conflicting information
Each participant completed multiple runs across two sessions.
Event files (*_events.tsv) contain trial-by-trial data such as:
onset, duration
trial_type (e.g., congruent, incongruent, neutral)
cue_type (e.g., center, double, spatial, none)
response_time, accuracy

Analysis Goals
Compute classic ANT metrics (e.g., alerting, orienting, and executive-control effects)
Model reaction times and accuracy with machine learning (e.g., regression, classification)
Identify subject-level patterns in attention and performance
Extend methods later to reward-learning or decision-making tasks

⚙️ Environment
To set up:
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
Main libraries (current or planned):
pandas, numpy, scipy
matplotlib, seaborn
scikit-learn
nibabel, nilearn, pybids (for optional neuroimaging work)

🚀 Next Steps
 Explore .tsv event files (inspect structure and variables)
 Merge multiple runs into a single trial-level dataset per subject
 Compute behavioural metrics and visualise distributions
 Build predictive models for reaction time or accuracy
 Document findings in reports/

📚 References
Grootswagers, T. (2020). A primer on running human behavioural experiments online.
McLeod, S. (2023). Experimental Method in Psychology.
Fan, J., McCandliss, B. D., Sommer, T., Raz, A., & Posner, M. I. (2002).
Testing the efficiency and independence of attentional networks. Journal of Cognitive Neuroscience, 14(3), 340–347.

Note: The repository may later include probabilistic reinforcement learning (PRL) datasets and cross-task modelling, using the same behavioural-ML pipeline developed here.