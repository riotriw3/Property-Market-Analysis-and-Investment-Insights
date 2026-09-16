# Property Market Analysis & Investment Insights

### Data Analysis of Property Listings in Jabodetabek

An exploratory data analysis project on property listings across Jabodetabek to identify data quality issues, property price patterns, common property characteristics, and potential investment opportunities to support business decision-making.

---

## 📌 Project Overview

This project was conducted as a Data Analyst case study for **PT Ray Pink Property Indonesia (RPPI)**.

The analysis aims to transform property listing data into business insights that can support management in understanding:

- The quality and consistency of the available property data
- Differences in property prices across cities
- Potential locations for future branch expansion
- The most commonly sold property characteristics
- Potential property candidates for investment within a maximum budget of Rp25 billion
- Additional insights that can support data-driven decision-making

The project focuses on **Exploratory Data Analysis (EDA)** and does not involve predictive modeling.

---

## 🎯 Business Questions

The analysis addresses the following business questions:

1. How is the quality of the property data?
2. What improvements can be recommended to improve data quality and consistency?
3. Are there differences in property prices across cities?
4. Which city could be considered for RPPI's next branch based on the available data?
5. What property characteristics appear most frequently in the dataset?
6. Which properties meet the defined criteria for a potential investment with a maximum budget of Rp25 billion?
7. What other valuable information can be extracted from the data?

---

## 📊 Dataset

The dataset contains property listings collected from five areas:

- Jakarta
- Depok
- Bogor
- Tangerang
- Bekasi

The original datasets were combined into a single dataset for analysis.

### Main Variables

| Variable | Description |
|---|---|
| `created_at` | Date when the property listing was created |
| `LT` | Land area (m²) |
| `LB` | Building area (m²) |
| `KT` | Number of bedrooms |
| `KM` | Number of bathrooms |
| `garasi` | Garage capacity |
| `carport` | Carport capacity |
| `lokasi` | Property location |
| `sertifikat` | Property certificate type |
| `listrik` | Electricity capacity |
| `hadap` | Property facing direction |
| `harga` | Property price |
| `URL` | Property listing URL |
| `deskripsi` | Property listing description |
| `wilayah` | Geographic area |

---

## 🧹 Data Preparation

The data preparation process included several steps:

### 1. Data Integration

Property datasets from Jakarta, Depok, Bogor, Tangerang, and Bekasi were combined into a single dataset.

### 2. Handling Empty Rows and Columns

Completely empty rows and columns were identified and removed.

### 3. Price Standardization

A difference in price units was identified across regions. Based on the assumption documented in the notebook, property prices were standardized into **million Rupiah** to make prices comparable across regions.

### 4. Data Type Validation

Data types were checked to identify inconsistencies, including non-numeric values in columns that should contain numerical property information.

### 5. Noise Handling

Non-numeric entries and irrelevant records were investigated and handled based on their context.

Certificate values were also standardized into two main categories:

- `SHM`
- `Lainnya`

### 6. Duplicate Check

The analysis found no duplicate records across the dataset.

### 7. Missing Value Analysis

Missing values were examined using percentage calculations and heatmap visualization.

Several missing values were handled based on assumptions documented in the analysis, including:

- `KM`, `garasi`, and `carport` → filled with `0`
- `sertifikat` → filled with `Lainnya`
- `deskripsi` and `hadap` → filled with `-`
- `listrik` → filled using the median value

### 8. Outlier Analysis

Property prices were examined using boxplots and analyzed by region.

The analysis separated data into datasets with and without identified price outliers to better understand the distribution of property prices.

---

## 🔎 Exploratory Data Analysis

The project uses several visualization techniques to explore the property market, including:

- Boxplots
- Catplots
- Scatter plots
- Heatmaps
- Geographic visualization using Folium
- Descriptive statistics

The analysis focuses on:

- Property price distribution
- Price differences across regions
- Property characteristics
- Relationship between building area and price
- Geographic distribution of property prices
- Potential investment candidates

---

## 💡 Key Insights

### 1. Data Quality

Several data quality issues were identified:

- High levels of missing values in several variables
- Differences in numerical units across regions
- Incomplete descriptions of some variables
- Inconsistent location formats across cities

For example, location information may be represented at different levels, such as districts, cities, or street names.

The analysis therefore recommends implementing standardized data formats, stronger data governance, and more detailed data documentation.

---

### 2. Property Price Differences

The analysis indicates a tendency for property prices to be higher in **Jakarta**, while relatively lower prices were observed in **Bogor, Bekasi, and Depok** based on the analyzed dataset.

This comparison was visualized using geographic and distribution-based visualizations.

---

### 3. Common Property Characteristics

The most frequently occurring property characteristics in the dataset were:

| Property Characteristic | Most Frequent Value |
|---|---:|
| Land Area | 60 m² |
| Building Area | 36 m² |
| Bedrooms | 2 |
| Bathrooms | 2 |
| Garage | 0 |
| Carport | 1 |

Therefore, the most frequently occurring property profile in the dataset is a house with **60 m² land area, 36 m² building area, 2 bedrooms, 2 bathrooms, no garage, and 1 carport**.

---

### 4. Investment Screening

To simulate a property investment scenario, the analysis applied predefined filters based on:

- 1–2 bathrooms
- 1–3 bedrooms
- 0–1 garage
- 1–2 carports
- 70–150 m² building area
- Maximum property price below Rp900 million
- Maximum total investment budget of Rp25 billion

The filtering process identified **37 properties** that met the defined criteria, with a combined listed price of approximately **Rp24.87 billion**.

These properties were treated as potential candidates based on the defined screening criteria rather than as guaranteed profitable investments.

---

### 5. Property Price Distribution

After separating identified regional outliers, the analyzed non-outlier dataset contained **604 properties**.

The resulting property prices ranged from approximately **Rp41 million to Rp15 billion** in the non-outlier dataset.

The notebook also notes that price distributions remain varied across the Jabodetabek regions.

---

## 📈 Business Recommendations

Based on the analysis, several recommendations were identified:

### Data Management

- Establish standardized data formats across regions.
- Implement stronger data governance practices.
- Define clearer data collection and maintenance guidelines.
- Provide more detailed definitions for each variable.

### Business Expansion

The notebook identifies **Depok** as a potential location for RPPI's next branch based on factors considered in the analysis, including geographic accessibility, relatively competitive property prices, and potential collaboration opportunities.

### Investment Screening

For an investment budget of up to Rp25 billion, the analysis provides a shortlist of properties that satisfy the predefined property characteristics and price criteria.

The shortlist should be treated as an initial screening result and further evaluated using additional investment factors before an actual investment decision.

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas** – Data manipulation and cleaning
- **NumPy** – Numerical computation
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Geopy** – Geocoding
- **Folium** – Geographic visualization
- **Google Colab** – Development environment

---

## 📂 Repository Structure

```text
Property-Market-Analysis-and-Investment-Insights/
│
├── CaseStudy01.ipynb
└── README.md
