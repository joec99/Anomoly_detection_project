# Ship Engine Anomaly Detection Project

## Project Overview
This project demonstrates a data-driven approach to detect anomalies in a ship's engine using key operational parameters. By identifying early signs of malfunction in components like engine RPM, lubrication oil pressure, fuel pressure, coolant pressure, lubrication oil temperature, and coolant temperature, this model aims to aid in proactive maintenance, enhancing safety and operational reliability.

## Business Context
Operational reliability of ships is critical for safety, efficiency, and cost-effectiveness. This project uses approximately 19,500 observations of engine functionality data to detect potential issues before they escalate into failures. Anomalies in engine parameters can be early indicators of potential malfunctions, providing a basis for timely interventions and preventative maintenance.

## Key Features
- **Data Exploration and Preparation**: Initial analysis includes identifying missing values, calculating statistical measures, and visualizing data distributions to inform the subsequent anomaly detection.
- **Outlier Detection Using Statistical and Machine Learning Approaches**: 
  - **IQR Method**: Flags outliers based on interquartile range across multiple features, with a 2.16% anomaly rate.
  - **One-Class SVM**: Optimized to classify around 3% of the data as anomalies using parameters `nu=0.03` and `gamma=0.01`.
  - **Isolation Forest**: Used with a contamination rate of 0.03, capturing 3% of data as anomalies.
- **Dimensionality Reduction and Visualization**: Principal Component Analysis (PCA) and t-SNE help visualize complex data and identify anomalies across engine parameters.

## Technical Skills Demonstrated
- Python programming (Pandas, NumPy, Scikit-learn)
- Data preprocessing and feature engineering
- Machine learning model implementation for anomaly detection (One-Class SVM, Isolation Forest)
- Data visualization and dimensionality reduction (Matplotlib, Seaborn, PCA, t-SNE)
- Evaluation and analysis of model performance in anomaly detection

## Project Structure
1. **Data Exploration and Preprocessing**: Handling missing values, data transformations, and initial visualizations.
2. **Outlier Detection**:
   - **IQR-based Method**: Identifies anomalies based on statistical thresholds.
   - **Machine Learning Models**: Implements One-Class SVM and Isolation Forest models to classify anomalous observations.
3. **Model Performance Analysis**: Evaluates and compares the efficacy of different models in detecting anomalies.
4. **Dimensionality Reduction and Visualization**: Applies PCA and t-SNE to enable 2D visualization of detected anomalies.
5. **Insights and Next Steps**: Summarizes findings and potential improvements for enhanced accuracy and business relevance.

## Key Findings
- **IQR Method**: Identified 2.16% of observations as anomalies, indicating the value of using multiple indicators.
- **One-Class SVM**: Detected 3% anomalies, with overlap in anomalies identified by both IQR and SVM models.
- **Isolation Forest**: Robustly identified 3% anomalies with consistent results across parameter settings.
- **Model Efficacy**: One-Class SVM provided precise control over anomaly detection rates, while Isolation Forest proved robust with minimal tuning requirements.
- **Visualization Insights**: Although PCA helps visualize anomalies, further dimensional analysis with t-SNE highlights local, non-linear relationships, enriching anomaly identification.

## Future Improvements
1. **Domain Expert Validation**: Collaborating with marine engineers to validate detected anomalies and refine feature selection or model parameters.
2. **Extended Visualization Techniques**: Using additional visualization methods to enhance interpretability, especially for complex, multi-dimensional anomaly patterns.
3. **Customized Anomaly Thresholding**: Fine-tuning anomaly thresholds based on expert insights to improve relevance and applicability in real-world maintenance contexts.

## Tools Used
- Python 
- Jupyter Notebook
- Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn, PCA, t-SNE for data visualization
