# Sales Data Analysis for a Commercial Store

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Insights and Recommendations](#key-insights-and-recommendations)
- [Installation](#installation)
- [Usage](#usage)
- [References](#references)
- [License](#license)
- [Contact](#contact)
- [Contributing](#contributing)

## Project Overview
This project performs a **sales data analysis** for a commercial store, focusing on sales trends, product performance, and customer behavior. Using **Exploratory Data Analysis (EDA)** and data visualizations, the analysis uncovers actionable insights to optimize business operations. The project is developed by **Brainwave Matrix Solutions**.

### Objectives
- Collect and analyze sales data to identify patterns and trends.
- Conduct EDA to explore sales distributions, top-performing products, and regional performance.
- Visualize findings using charts and graphs for clear communication.

---

## Dataset
The dataset contains **185,950 sales records** from a commercial store, detailing individual transactions with the following columns:

- **Order ID**: Unique identifier for each order.
- **Product**: Name of the product sold.
- **Quantity Ordered**: Number of units ordered.
- **Price Each**: Price per unit of the product.
- **Order Date**: Date and time of the order.
- **Purchase Address**: Delivery address of the order.
- **Month**: Month of the sale (extracted from Order Date).
- **Sales**: Total sales value (Quantity Ordered * Price Each).
- **City**: City where the order was placed.
- **Hour**: Hour of the day when the order was placed.

### Dataset Statistics
- **Total Records**: 185,950
- **Shape**: (185,950 rows, 11 columns)
- **Missing Values**: None
- **Key Metrics**:
  - Average Sales: $185.49
  - Average Quantity Ordered: 1.12 units
  - Price Range: $2.99 - $1,700.00

The dataset is stored in `Sales Data.csv`.

---

## Methodology

### Data Preprocessing
1. Removed the unnecessary `Unnamed: 0` index column.
2. Dropped duplicate rows to ensure data integrity.
3. Converted data types:
   - `Order Date` to datetime.
   - `Price Each`, `Quantity Ordered`, and `Sales` to appropriate numeric types.

### Exploratory Data Analysis (EDA)
- Analyzed sales trends by month, hour, and city.
- Investigated product performance through quantities sold and revenue generated.
- Examined customer behavior via purchase timing and regional distribution.

### Tools and Libraries
- **Python Libraries**: 
  - `pandas` for data manipulation.
  - `numpy` for numerical operations.
  - `matplotlib` and `seaborn` for visualizations.

### Visualizations
- **Revenue Distribution by City**: Violin plots to show revenue spread across cities.

---

## Key Insights and Recommendations

### Key Insights
1. **Top-Performing Products/Regions**:
   - Certain products and cities consistently drive higher revenue.
2. **Sales Patterns**:
   - Peak sales occur during specific hours and months, likely tied to external factors (e.g., holidays).
3. **Impact of Discounts**:
   - Discounts boost sales volume but may reduce profit margins if not managed carefully.
4. **Customer Preferences**:
   - High-demand products and regional sales patterns reveal customer preferences.

### Recommendations
1. **Focus on High-Revenue Categories**:
   - Allocate resources to top-performing products and regions for sustained growth.
2. **Expand in Top-Performing Regions**:
   - Target high-sales cities with localized promotions and expanded operations.
3. **Targeted Discount Strategies**:
   - Use data-driven discounts to balance sales volume and profitability.
4. **Prepare for Peak Periods**:
   - Align inventory and marketing with identified high-demand times.

---

## Installation

### Prerequisites
- Python 3.8+
- Required libraries:
  ```bash
  pip install pandas numpy matplotlib seaborn
  ```

## Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/Parmod2310/Commercial-Store.git
cd Commercial-Store-
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Place the dataset:
   
- Add `Sales Data.csv` to the project root or a `data/` directory.

---

## Usage

### Running the Analysis
Run the main analysis script:
```bash
Commercial_store.ipynb
```

This script loads the dataset, performs preprocessing, conducts EDA, and generates visualizations(e.g. revenue by city). 

### Example Visualization
To generate a revenue distribution plot by city: 

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

sales = pd.read_csv("Sales Data.csv")
plt.figure(figsize=(10, 6))
sns.violinplot(x='City', y='Sales', data=sales, palette='Set3')
plt.title('Revenue Distribution by City')
plt.xlabel('City')
plt.ylabel('Revenue')
plt.xticks(rotation=45)
plt.savefig('revenue_by_city.png')  # Save to file
print("Plot saved as 'revenue_by_city.png'")
plt.show()  # Attempt to display (works if GUI is available)
```

---

## References
- Sales Data Source *(Update with actual source if available)*
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Seaborn Documentation](https://seaborn.pydata.org/)

---

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Contact
For questions or contributions, please reach out via [p921035@gmail.com](mailto:p921035@gmail.com).

---

## Contributing
Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.
