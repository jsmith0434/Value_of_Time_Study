---

# 🚗 I-405 Tollway Value of Time Study

### 📊 Project Overview
This project served as the senior capstone for **Washington State University’s Data Analytics program**. The study analyzes driver behavior and economic decision-making on the **Interstate-405 express toll lanes (ETL)** during 2019. The core objective was to calculate the **Value of Time (VOT)**—the monetary amount a driver is willing to pay to reduce travel time—and to understand how travel time variability influences those decisions.

Using real-world datasets from the **Washington State Department of Transportation (WSDOT)**, this research models the complex relationships between toll rates, vehicle volume, speed, and commute reliability.

---

### 🧠 Methodology & Technical Approach
The analysis utilized a robust data pipeline to convert raw traffic telemetry into economic insights:

* **Mathematical Modeling**: Implemented the **Small & Yan (2001)** VOT equation, factoring in operational costs such as fuel prices and vehicle depreciation.
* **Travel Time Variability**: Calculated the standard deviation of travel times at 15-minute intervals. High variability was identified as a primary driver for toll lane adoption.
* **Statistical Validation**: Applied **Shapiro-Wilk normality tests** and **Tukey Contrast** multiple comparison tests to ensure the statistical significance of speed and volume differences between general-purpose and toll lanes.
* **Data Wrangling**: Managed large-scale WSDOT telemetry, tracking vehicle groups across entry points to eliminate double-counting and accurately estimate segment-specific volumes.

---

### 📂 Repository Structure

| File | Description |
| :--- | :--- |
| **`final_artifact.rmd`** | The R Markdown source for the **Flexdashboard** and core visualizations, including toll lane speed distributions and time-savings maps. |
| **`final_project_calculations.rmd`** | The heavy-lifting script used for data cleaning, VOT equation implementation, and statistical modeling. |
| **`Value of Time Project Report.pdf`** | The comprehensive final report detailing the background, literature review, results, and executive summary. |

---

### 📈 Key Findings
* **Southbound Urgency**: Southbound commuters demonstrated the highest Value of Time at **$34.31/hr**, driven by higher travel time variability and average speeds frequently dropping below 45 mph.
* **Reliability vs. Speed**: The study confirmed that "reliability" (consistency of travel time) is often a greater motivator for paying tolls than "speed" alone.
* **Average Savings**: On average, toll lane usage saved commuters **19 minutes** during peak travel windows compared to general-purpose lanes.

---

### 🔮 Future Research & Extensions
* **COVID-19 Impact Analysis**: A longitudinal study comparing this 2019 baseline to 2020–2022 data to see how "flattened" peak hours have altered the economic value of reliability.
* **Predictive Modeling**: Leveraging the identified exponential relationship between time savings and toll rates to develop a Machine Learning model that predicts ETL usage based on weather or incident data.
* **Elasticity by Vehicle Type**: Integrating data to distinguish between single-occupant vehicles and transit to determine if HOV requirements change the VOT threshold.

---

### 📌 How to Run
1.  **Environment**: Ensure RStudio is installed with the following libraries: `tidyverse`, `flexdashboard`, `plotly`, and `scales`.
2.  **Data Setup**: Place the WSDOT 5-minute interval datasets in the `/data` directory.
3.  **Execution**: 
    * Run `final_project_calculations.rmd` first to generate the cleaned data frames and statistical summaries.
    * Open `final_artifact.rmd` and click **"Run Document"** to launch the interactive Flexdashboard.

---

