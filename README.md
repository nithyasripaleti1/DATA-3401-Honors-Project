# Impact of Amazon Deforestation on Bird Diversity  
*Honors Data Science Project*

## Project Overview
This project analyzes the relationship between deforestation in the Amazon Basin and changes in bird species richness using large-scale biodiversity and environmental datasets. The analysis integrates bird occurrence records from the Global Biodiversity Information Facility (GBIF) with satellite-derived forest loss data from Global Forest Watch (GFW) to explore how land-use change and sampling effort influence observed biodiversity trends.

The project emphasizes the importance of accounting for observation bias when interpreting ecological patterns from opportunistic data sources.


## Research Questions
- How have deforestation rates in the Amazon Basin changed over time?
- How does bird species richness vary temporally and regionally across the Amazon?
- How does accounting for sampling effort affect the observed relationship between deforestation and biodiversity?


## Data Sources
- **Global Biodiversity Information Facility (GBIF)**  
  Bird species occurrence records (2000–2024)
- **Global Forest Watch (GFW) Data API**  
  Annual forest cover loss estimates derived from satellite imagery (2001–2024)

After cleaning and spatial filtering to the Amazon Basin, the final biodiversity dataset contained approximately **2 million records**.


## Methodology

### 1. Data Cleaning & Preprocessing
- Filtered GBIF bird occurrence records to the Amazon Basin using a geographic bounding box
- Removed duplicates and records with missing spatial or temporal information
- Aggregated records annually and assigned observations to broad Amazon regions (West, Central, East)

### 2. Species Richness & Sampling Effort
- Computed annual bird species richness (unique species per year)
- Quantified observation effort using annual record counts
- Derived an effort-normalized richness metric (species per 10,000 records) to correct for uneven sampling intensity

### 3. Statistical Analysis
- Modeled temporal trends in species richness and observation effort
- Performed linear regression analysis to examine relationships between forest loss and:
  - Raw species richness
  - Effort-normalized species richness
- Compared regional trends across West, Central, and East Amazon regions

### 4. Visualization
- Created time-series plots of richness, effort, and forest loss
- Visualized regional richness trends and spatial sampling density
- Highlighted how sampling bias can invert apparent ecological relationships


## Key Findings
- Raw bird species richness increased over time and was positively correlated with forest loss, reflecting increased observation effort in accessible and deforested areas.
- After normalizing for sampling effort, species richness showed a **negative association with forest loss**, indicating potential biodiversity decline masked by observation bias.
- Regional analyses revealed similar richness trends across Amazon regions, driven primarily by changes in sampling intensity rather than contrasting ecological trajectories.


## Tools & Technologies
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, scikit-learn  
- **Environment:** Jupyter Notebook  


## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/nithyasripaleti1/DATA-3401-Honors-Project.git
2. Install dependencies:
   pip install pandas numpy matplotlib seaborn
3. Launch Jupyter Notebook

## Why This Project Matters

Large biodiversity databases enable powerful large-scale analyses but are highly susceptible to sampling bias. This project demonstrates how simple effort-normalization and transparent statistical modeling can substantially change ecological interpretations, highlighting best practices for responsible environmental data analysis.
