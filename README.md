# **Stream Analytics Assignment**

This repository contains the code, documentation, and related files for **Stream Analytics Assignment - 1**, completed as part of the **CSL7970** course under the guidance of **Nitin Awathare** during **Trimester III**.

---

## **Project Details**

### **Course Information**
- **Course**: Stream Analytics
- **Assignment Name**: Assignment - 1
- **Course Code**: CSL7970
- **Guide**: Nitin Awathare
- **Trimester**: III

### **Team Members**
- **Niraj Bhagchandani** - Roll Number: G23AI2087
- **Bhavesh Arora** - Roll Number: G23AI2126

---

## **Repository Contents**

This repository includes the following files and resources:

### 1. **Code Files**
- **`Assignment-1.ipynb`**: 
  - Jupyter Notebook containing all the Python code for data loading, preprocessing, analysis, and visualization.
  - Key operations include:
    - Filtering TCP traffic.
    - Identifying anomalous nodes.
    - Classifying nodes using **Very Fast Decision Trees (VFDT)** and **KNN**.
    - Generating insightful visualizations.
  
### 2. **Documentation**
- **`Assignment-1.docx`**:
  - Word document containing the formal report for the assignment, including:
    - Headers and footers with course details.
    - Summarized insights and conclusions.
    - Visualizations and tabular results.

- **`Assignment-1.pdf`**:
  - PDF version of the Word document for easy sharing and accessibility.

### 3. **Snapshots**
- **`/snapshots/`**:
  - Folder containing relevant snapshots of the analysis and visualizations generated during the assignment.

---

## **Key Features**

This project focuses on **TCP traffic analysis and anomaly detection** using Python. Below are the major tasks performed:

### **1. Data Preprocessing**
- Loaded data from:
  - Local CSV file.
  - AWS S3 bucket (with progress monitoring using `tqdm`).
- Cleaned column names and replaced invalid values in `duration` to avoid division by zero.
- Computed `packets_per_second` for each node.

### **2. Classification**
- **Very Fast Decision Trees (VFDT)**:
  - Used the `river` library to train a streaming decision tree model incrementally.
- **KNN Classifier**:
  - Implemented optimized K-Nearest Neighbors classification using `ball_tree` algorithm for efficient performance.

### **3. Anomaly Detection**
- Identified anomalous nodes based on a predefined threshold for `packets_per_second`.
- Highlighted key characteristics of anomalies, including:
  - Traffic distribution by source IP.
  - Percentage of anomalous packets relative to total traffic.

### **4. Visualization**
- Generated insightful visualizations:
  - **Traffic class distribution**: Bar plot.
  - **Normal vs Anomalous Nodes**: Scatter plot.
  - **IP group analysis**: Bar chart of normal vs anomalous IP groups.

---

## **Setup Instructions**

### **1. Prerequisites**
Ensure you have the following libraries installed:
- **Python 3.7+**
- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`
- `tqdm`
- `river`

Install the required libraries using:
```bash
pip install numpy pandas matplotlib scikit-learn tqdm river
```

## Results and Insights

### Key Results:
- Successfully classified nodes into **traffic classes**: Very Low, Low, Medium, and High.
- Detected **anomalous nodes** with high traffic rates.
- Visualized and analyzed traffic behavior across source IPs and IP groups.

---

## Authors
- **Niraj Bhagchandani** (G23AI2087)
- **Bhavesh Arora** (G23AI2126)

---

## Acknowledgments
- **Guide**: Nitin Awathare
- **Course**: CSL7970 - Stream Analytics
- **Institution**: Indian Institute of Technology - Jodhpur

---

## License
This project is licensed under the [MIT License](LICENSE).

Feel free to contribute, raise issues, or share feedback!
