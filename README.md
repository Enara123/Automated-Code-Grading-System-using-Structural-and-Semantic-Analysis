# Automated Java Code Grading using Structural and Semantic Analysis

## Overview

This project presents a proof-of-concept automated code grading system designed to evaluate Java programming assignments. The system aims to improve grading reliability and reduce dependence on problem-specific rules by combining both structural and semantic analysis of code.

Traditional automated grading systems rely heavily on predefined test cases or static rules, limiting their ability to generalize across different problems. This project addresses that limitation by integrating Abstract Syntax Tree (AST)-based structural analysis with semantic embeddings generated using GraphCodeBERT. These features are used to train a deep learning model that predicts a numerical grade between 0–100.

The system is deployed as a Streamlit web application, allowing users to upload Java code and receive instant grading predictions.

----

## Features

* Extracts structural features using AST parsing (e.g., loops, methods, nesting depth)
* Generates semantic embeddings using GraphCodeBERT
* Combines structural and semantic features into a unified representation
* Predicts grades using a Feed-Forward Neural Network (FNN)
* Supports grading across different problem types (problem-independent approach)
* Interactive web interface built with Streamlit

----

## System Architecture

![Proposed Architecture Diagram](https://github.com/user-attachments/assets/23c90608-f9ec-415b-a8f5-8dd4bda57d99)
<!--
The system follows a modular pipeline:

1. **Input**: Java code submission
2. **Preprocessing**: Code cleaning and formatting
3. **Feature Extraction**:

   * Structural features via AST
   * Semantic features via GraphCodeBERT
4. **Feature Fusion**: Combine extracted features with metadata (e.g., difficulty level)
5. **Model Prediction**: Neural network predicts a grade (0–100)
6. **Output**: Display predicted grade via Streamlit interface
-->
----

## Tech Stack

* **Programming Language**: Python
* **Frameworks/Libraries**:

  * PyTorch (model development)
  * Streamlit (web application)
  * Javalang (AST parsing)
  * Transformers / GraphCodeBERT (semantic analysis)
* **Other Tools**: NumPy, Pandas, Scikit-learn

----

## Results

The model was evaluated using standard regression metrics:

* **MAE**: 18.68
* **MSE**: 569.04
* **RMSE**: 23.85
* **R² Score**: -0.37

The results indicate that while the model captures some patterns in grading, overall predictive performance is limited. Scatter plot analysis shows weak correlation between predicted and actual grades.

This is primarily due to the small dataset (384 submissions), making this project a proof-of-concept rather than a production-ready system.

----

## Limitations

* Limited dataset size affects model generalization
* High-dimensional feature space with relatively simple model
* Model struggles to accurately learn grading patterns
* Currently supports only Java code
----

## Future Improvements

* Use a larger and more diverse dataset (e.g., full CodeNet dataset)
* Experiment with advanced architectures (e.g., transformers, LLMs)
* Incorporate grading rubrics for better alignment with human evaluation
* Add automated feedback generation (not just grades)
* Improve model performance and generalization

----

## Author

**Siluni Enara Koperahewa**
* Final Year Software Engineering Undergraduate
* Coventry University

----

## License

This project is for academic and research purposes.
