
# ML-TestPrioritization: Automated Test Case Prioritization Using Machine Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-orange.svg)

## Overview

ML-TestPrioritization is a data-driven solution to optimize software testing by prioritizing test cases using machine learning. In resource-constrained environments, selecting the most effective tests is critical. This project leverages a Random Forest Classifier to identify high-value test cases based on bug detection rates and business impact. It includes a smart test selection engine, ROI analysis, and actionable QA recommendations to maximize test coverage, reduce testing time, and improve efficiency.

**Key Features**:
- Generates a realistic dataset of 2,500 test cases with attributes like test type, priority, complexity, and business impact.
- Performs exploratory data analysis (EDA) with visualizations to uncover patterns in test case performance.
- Trains a Random Forest Classifier to prioritize high-value tests.
- Implements a smart test selection engine to optimize test execution within time constraints (e.g., 4 hours).
- Conducts ROI analysis comparing smart selection to full testing.
- Provides actionable recommendations for automation, maintenance, coverage, and performance optimization.

This project is ideal for software testers, QA engineers, and data scientists interested in applying machine learning to software quality assurance.

## Dataset

The dataset is synthetically generated with realistic attributes:
- **Columns**: `test_id`, `test_type`, `priority`, `component`, `complexity`, `execution_time_min`, `times_executed`, `bugs_found`, `bug_detection_rate`, `last_updated_days`, `automation_feasible`, `business_impact`, `requirements_covered`, `environment_dependencies`
- **Size**: 2,500 test cases
- **Key Metrics**:
  - Total bugs found: ~5,000 (varies with random seed)
  - Average bug detection rate: ~0.15
  - Automation potential: ~60% of tests are automation-feasible

The dataset simulates real-world QA scenarios with relationships between test complexity, priority, and bug-finding probability.

## Installation

To run this project locally, follow these steps:

### 1. Clone the Repository:
```bash
git clone https://github.com/khawjaahmad/ML-TestPrioritization.git
cd ML-TestPrioritization
```

### 2. Install Dependencies:
Ensure Python 3.8+ is installed, then install required libraries:
```bash
pip install -r requirements.txt
```

**Content of requirements.txt**:
```
pandas
numpy
matplotlib
seaborn
scikit-learn
```

### 3. Run the Notebook:
Open the Jupyter notebook in Jupyter or Kaggle:
```bash
jupyter notebook ML_TestPrioritization.ipynb
```

## Usage

- **Data Generation**: Creates a synthetic dataset of 2,500 test cases with realistic attributes.
- **Exploratory Data Analysis**: Visualizes bug detection rates, test priorities, component performance, and feature importance using bar charts, pie charts, and scatter plots.
- **Model Training**: Trains a Random Forest Classifier to predict high-value test cases (high bug detection or business impact).
- **Smart Test Selection**: Selects optimal tests within a time constraint (e.g., 4 hours) using a weighted scoring system combining ML predictions, bug detection rates, business impact, and execution time.
- **ROI Analysis**: Compares the cost and value of smart test selection vs. full testing.
- **Recommendations**: Generates actionable QA recommendations for automation, maintenance, coverage, and performance.

**View the notebook on [Kaggle](https://www.kaggle.com/khawjaahmad)**

## Key Insights

- **Highest Bug Detection**: Integration and API tests have the highest bug detection rates.
- **Problematic Components**: Payment and Authentication components yield the most bugs due to high business impact.
- **Automation Potential**: ~60% of tests are feasible for automation, with UI tests showing lower automation rates.
- **Execution Time**: Average test execution time is ~10–15 minutes.
- **Feature Importance**: Bug detection rate and business impact are top predictors of high-value tests.

## Model Performance

The Random Forest Classifier achieves robust performance:
- **Accuracy**: ~85–90% (varies with random seed)
- **Precision/Recall**: Detailed in the notebook’s classification report
- **Feature Importance**: Visualized to highlight key drivers like bug detection rate and business impact

## Smart Test Selection

The smart test selection engine optimizes test execution:
- Selects ~200–300 tests within a 4-hour window
- Achieves ~30–50% higher bug detection rates compared to random selection
- Reduces testing time while maintaining quality

## ROI Analysis

The ROI analysis quantifies efficiency gains (based on $50/hour tester rate and $1,000/bug fix cost):

**Smart Selection (e.g., 4 hours):**
- Cost: ~$200
- Bugs found: ~1,000
- ROI: ~400–500%

**Full Testing:**
- Cost: ~$1,000–$1,500
- Time: ~20–30 hours
- Bugs found: ~5,000

**Efficiency Gains**:
- Time saved: ~80–85%
- Bug detection efficiency: ~2–3x higher than proportional testing time

## Actionable Recommendations

The notebook provides tailored QA recommendations:
- **Automation**: Automate frequent, time-consuming tests to save hours per cycle
- **Maintenance**: Review stale tests (>180 days old) to improve relevance
- **Coverage**: Increase testing for under-tested components (e.g., Database, Reporting)
- **Performance**: Optimize slow-running tests to reduce execution time

## Future Improvements

- Incorporate real-world test case data
- Experiment with advanced models like XGBoost
- Integrate with CI/CD pipelines for real-time test prioritization
- Expand to include defect prediction

## Contributing

Contributions are welcome! Please:

1. Fork the repository  
2. Create a feature branch:  
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit changes:  
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to the branch:  
   ```bash
   git push origin feature/your-feature
   ```
5. Open a pull request

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contact

For questions or feedback, reach out via [GitHub Issues](https://github.com/khawjaahmad/ML-TestPrioritization/issues) or connect on [Kaggle](https://www.kaggle.com/khawjaahmad).

---

*Built with ❤️ by Ahmad for the QA and Data Science communities.*
```
