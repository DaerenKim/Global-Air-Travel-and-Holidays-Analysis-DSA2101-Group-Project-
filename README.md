# Global Air Travel and Holidays Analysis

This project investigates how holidays and regional differences shape global air travel patterns using publicly available datasets. We analyze seasonal variations, domestic-to-international flight ratios, and regional air traffic trends over time with a combination of choropleth maps, line plots, and bubble plots.

---

## Overview

Air travel patterns are influenced by multiple factors including holidays, geography, economics, and connectivity. This project focuses on three main questions:

1. How do holidays affect air passenger volumes globally?  
2. How do monthly air travel patterns vary across continents?  
3. How do domestic vs international flight ratios differ by continent over time?

We use three visualization approaches to explore these questions:

1. **Bivariate Choropleth Maps:** Show the relationship between average quarterly air passenger volumes and average holidays per country.  
2. **Line Plots by Continent:** Display monthly air passenger trends over multiple years to understand seasonal patterns.  
3. **Bubble Plots:** Examine the domestic-to-international flight ratios per continent, highlighting shifts in regional travel behaviors.

---

## Data Sources

All datasets are publicly available from [TidyTuesday](https://github.com/rfordatascience/tidytuesday):

- **Global Holidays Dataset:**  
  [https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2024/2024-12-24/global_holidays.csv](https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2024/2024-12-24/global_holidays.csv)  

- **Monthly Passengers Dataset:**  
  [https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2024/2024-12-24/monthly_passengers.csv](https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2024/2024-12-24/monthly_passengers.csv)  

Example Python function to import the data:

```python
import pandas as pd

def import_data() -> tuple[pd.DataFrame, pd.DataFrame]:
    holidays_data = pd.read_csv("https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2024/2024-12-24/global_holidays.csv")
    passengers_data = pd.read_csv("https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2024/2024-12-24/monthly_passengers.csv")
    print("Imported: Holidays Data + Passengers Data")
    return holidays_data, passengers_data

holidays_df, passengers_df = import_data()
```

## Setup and Configuration

**Python Version Requirement:**  
This project is compatible **only with Python 3.12**. Python 3.13 or higher is not supported.

### 1. Create a Python 3.12 Virtual Environment
```bash
python3.12 -m venv airtravel_env
source airtravel_env/bin/activate   # Linux/Mac
# OR
airtravel_env\Scripts\activate      # Windows
```

## 2. Install Required Libraries

Using a `requirements.txt`:

```bash
pip install -r requirements.txt
```

## 3. Run the Analysis

1. Preprocess datasets as described in the scripts.  
2. Run the visualization scripts in the following order:
   - **Bivariate Choropleth Map**  
   - **Line Plot by Continent**  
   - **Bubble Plot: Domestic vs International Ratio**  

Visualizations can be displayed inline in Jupyter Notebook or saved with `plt.savefig()`.

---

## Key Findings

### 1. Bivariate Choropleth Map
- The United States and China consistently show high air traffic (bright purple), reflecting large domestic markets and extensive connectivity.  
- Seasonal peaks observed in Russia and Turkey highlight strong holiday-driven travel patterns.  
- Europe shows a mixture of hub-driven traffic (Germany, UK) and tourism-driven patterns (Spain).

### 2. Line Plot by Continent
- North America, Asia, and Europe show strong seasonal peaks corresponding to school and national holidays.  
- Asia shows a growing trend in air passengers from 2013 onward, reflecting increasing economic growth and connectivity.  
- Africa, Oceania, and South America have muted seasonal variations due to smaller markets, higher costs, and lower connectivity.

### 3. Bubble Plot: Domestic vs International Ratio
- Large, dispersed continents (North America, Asia, Oceania) have high domestic-to-international ratios due to long distances between cities.  
- Europe shows lower ratios, reflecting compact geography and seamless international travel through the Schengen Area.  
- Over time, Asia’s ratio decreases as international travel grows faster than domestic travel.

**Overall:** Holidays amplify regional travel patterns but do not fully determine global air travel. Geography, economic growth, and connectivity are equally important factors.

---

## Team Contributions

| Plot | Team Members |
|------|--------------|
| Bivariate Choropleth Map | Ng Chong Xuan, Ong Wei Zheng, Julian |
| Line Plot by Continent | Eugene Poon Wen Teng, Jin Suxin |
| Bubble Plot: Domestic vs International Ratio | Daeren Kim Boon Hong, Siah Jin Thau |

