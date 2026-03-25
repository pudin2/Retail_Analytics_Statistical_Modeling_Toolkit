# Retail Analytics and Statistical Modeling Toolkit

## Overview
This repository contains a set of Jupyter notebooks for exploratory analysis, data quality assessment, business visualization, and statistical modeling over a retail orders/products dataset. The project focuses on product portfolio behavior, logistics and freight patterns, pricing relationships, regional comparisons, and category-market dependency.

The notebooks are designed as complementary analyses over the same base dataset, moving from data understanding and governance checks to descriptive analytics and hypothesis testing.

## Recommended repository name
**Retail_Analytics_Statistical_Modeling_Toolkit**

### Other strong alternatives
- `Retail_Operations_Analytics_Lab`
- `Retail_Logistics_Product_Analytics`
- `Retail_Business_Statistics_Portfolio`
- `Retail_Data_Quality_And_Statistical_Insights`

My main recommendation is **Retail_Analytics_Statistical_Modeling_Toolkit** because it covers the full scope of the repository: data quality, exploratory analysis, business visualization, logistics, and inferential statistics.

## Main objectives
- Assess raw retail data quality before analysis.
- Explore the commercial structure of the product portfolio.
- Visualize regional and category-level retail patterns.
- Study the relationship between price, freight, weight, and product dimensions.
- Compare freight behavior across seller regions.
- Apply inferential techniques such as z-test, t-test, ANOVA, and chi-square.

## Repository contents

### Notebooks
- `Retail_Data_Quality_Governance_Assessment.ipynb`  
  Review of data types, null values, duplicates, and basic governance/cleaning steps on the raw dataset.

- `Retail_Product_Portfolio_Exploratory_Analysis.ipynb.ipynb`  
  Exploratory analysis of product categories, univariate frequencies, cumulative distributions, cross-tabulations, and descriptive statistics.

- `Retail_Product_Portfolio_Analysis_Using_Business_Visualization_Techniques.ipynb`  
  Business-oriented visualizations including bar charts, grouped bars, stacked bars, normalized stacked bars, histograms, boxplots, treemaps, and sunburst charts.

- `Retail_Pricing_Logistics_Correlation_Analysis.ipynb`  
  Correlation and scatter-plot analysis among price, freight value, product weight, area, and volume.

- `Retail_Logistics_Freight_Regional_Comparison_Analysis.ipynb`  
  Regional freight comparison using descriptive statistics, confidence intervals, mean comparisons, and a z-test between selected departments.

- `Retail_Logistics_Freight_Regional_TTest_Analysis.ipynb`  
  Two-group comparison of freight averages using Student's t-test.

- `Retail_Logistics_Freight_Regional_ANOVA_Analysis.ipynb`  
  Multi-group mean comparison using one-way ANOVA over selected departments/regions.

- `Retail_Market_Structure_Category_Dependency_Analysis.ipynb`  
  Category-vs-region dependency analysis using contingency tables and chi-square testing.

### Data files
The notebooks reference the following datasets:
- `Ordenes_productos_C1_M2_Raw.csv` -> raw source dataset
- `Ordenes_productos_C1_M2.csv` -> cleaned/processed dataset
- Data dictionary file -> variable descriptions, semantic meaning, and field interpretation

> Note: The notebooks load CSV files with `sep=';'` and `encoding='latin-1'`.

## Analytical scope
The repository covers the following analytical dimensions:

### 1. Data quality and governance
- Data type inspection
- Missing value detection
- Duplicate detection and removal
- Basic cleaning actions
- Fitness-for-analysis validation

### 2. Exploratory retail analytics
- Category frequency analysis
- Relative and cumulative frequency distributions
- Bivariate frequency tables
- Descriptive statistics for price and product attributes

### 3. Business visualization
- Seller-region concentration
- Product category composition by region
- Distribution views for price and product dimensions
- Portfolio composition through interactive charts

### 4. Logistics and pricing analysis
- Freight averages by seller department
- Price/freight/weight relationships
- Derived variables such as area and volume
- Regional freight behavior comparison

### 5. Inferential statistics
- **Z-test** for mean comparison between two groups
- **T-test** for mean comparison under alternative assumptions
- **One-way ANOVA** for multiple-group comparison
- **Chi-square test** for categorical dependency assessment

## Dataset themes inferred from the notebooks
The analysis appears to use fields such as:
- `orden_id`
- `producto_id`
- `nombre_categoria_producto`
- `precio`
- `valor_flete`
- `peso_g_producto`
- `longitud_cm_producto`
- `altura_cm_producto`
- `ancho_cm_producto`
- `departamento_vendedor`
- `ciudad_vendedor`
- `codigo_postal_vendedor`
- `fecha_envio_limite`

## Suggested project structure
```text
Retail_Analytics_Statistical_Modeling_Toolkit/
│
├── data/
│   ├── raw/
│   │   └── Ordenes_productos_C1_M2_Raw.csv
│   ├── processed/
│   │   └── Ordenes_productos_C1_M2.csv
│   └── dictionary/
│       └── data_dictionary.csv
│
├── notebooks/
│   ├── Retail_Data_Quality_Governance_Assessment.ipynb
│   ├── Retail_Product_Portfolio_Exploratory_Analysis.ipynb
│   ├── Retail_Product_Portfolio_Analysis_Using_Business_Visualization_Techniques.ipynb
│   ├── Retail_Pricing_Logistics_Correlation_Analysis.ipynb
│   ├── Retail_Logistics_Freight_Regional_Comparison_Analysis.ipynb
│   ├── Retail_Logistics_Freight_Regional_TTest_Analysis.ipynb
│   ├── Retail_Logistics_Freight_Regional_ANOVA_Analysis.ipynb
│   └── Retail_Market_Structure_Category_Dependency_Analysis.ipynb
│
├── README.md
└── requirements.txt
```

## Recommended execution order
1. `Retail_Data_Quality_Governance_Assessment.ipynb`
2. `Retail_Product_Portfolio_Exploratory_Analysis.ipynb.ipynb`
3. `Retail_Product_Portfolio_Analysis_Using_Business_Visualization_Techniques.ipynb`
4. `Retail_Pricing_Logistics_Correlation_Analysis.ipynb`
5. `Retail_Logistics_Freight_Regional_Comparison_Analysis.ipynb`
6. `Retail_Logistics_Freight_Regional_TTest_Analysis.ipynb`
7. `Retail_Logistics_Freight_Regional_ANOVA_Analysis.ipynb`
8. `Retail_Market_Structure_Category_Dependency_Analysis.ipynb`

## Environment and dependencies
Suggested Python version:
- Python 3.10+

Main libraries used across the notebooks:
- `pandas`
- `numpy`
- `matplotlib`
- `plotly`
- `scipy`
- `statsmodels`
- `jupyter`

Example installation:
```bash
pip install pandas numpy matplotlib plotly scipy statsmodels notebook
```

## How to run
1. Clone the repository.
2. Place the raw, cleaned, and dictionary files in the corresponding folders.
3. Open Jupyter Notebook or JupyterLab.
4. Update paths if needed.
5. Execute notebooks in the suggested order.

## Example use cases
- Evaluate whether freight costs differ significantly across seller regions.
- Explore which product categories dominate the portfolio.
- Measure whether logistics variables are correlated with price.
- Check if category distribution depends on seller region.
- Build an academic or business case combining descriptive and inferential analytics.

## Potential improvements
- Standardize notebook naming and folder structure.
- Add a single reusable data-loading utility.
- Incorporate assumptions checks for statistical tests.
- Add post-hoc tests after ANOVA, such as Tukey HSD.
- Add automated data quality reports.
- Export visualizations and results into presentation-ready outputs.
- Add `requirements.txt` and environment reproducibility instructions.

## Notes
- Some notebooks assume exact column names and direct file paths.
- At least one notebook file currently appears duplicated in its extension (`.ipynb.ipynb`); renaming it would improve cleanliness.
- To make the repository more production-ready, consider moving datasets into `data/raw` and `data/processed` and adjusting all notebook paths accordingly.

## License
Define the license according to your intended use: academic, internal, or open-source distribution.
