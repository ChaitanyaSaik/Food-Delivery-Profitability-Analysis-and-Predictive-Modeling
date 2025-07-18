# Food Delivery Profitability Analysis and Predictive Modeling

## Project Overview
This project presents a comprehensive analysis of food delivery profitability. It aims to understand the revenue and cost components of each transaction and leverages predictive modeling to forecast profitability in the competitive food delivery industry.

## Objective
- Identify key revenue streams and cost factors.
- Clean and preprocess transaction data.
- Calculate the true profit for each order.
- Visualize cost distributions and profit patterns.
- Conduct inferential analysis (hypothesis testing, A/B testing).
- Build predictive models to forecast profitability.
- Provide actionable business strategies.

## Key Variables
- **Order Value**: Revenue earned from each transaction.
- **Delivery Fee**: Cost of delivering the food.
- **Commission Fee**: Percentage of the order paid by the restaurant.
- **Payment Processing Fee**: Fees from digital transactions.
- **Refunds/Chargebacks**: Refunded or lost amounts.
- **Discounts and Offers**: Revenue-reducing incentives.
- **Delivery Duration**: Time from order to delivery.
- **Total Cost**: Sum of Delivery Fee, Discounts, and Payment Fee.
- **Profit**: Commission Fee - Total Cost.

## Data Sources
The dataset includes detailed information about food orders such as order value, delivery fees, commissions, discounts, and payment methods.

## Data Collection and Preprocessing
- **Missing Data Handling**: Replaced nulls in "Discounts and Offers" with "No Discount".
- **Data Type Conversion**: Converted time columns to datetime format.
- **Feature Engineering**:
  - Delivery Duration (in minutes)
  - Normalized Discounts
  - Total Cost = Delivery Fee + Discounts + Payment Processing Fee
  - Profit = Commission Fee - Total Cost
- **Column Dropping**: Removed identifiers after calculations.
- **One-Hot Encoding**: Applied to categorical payment methods.

## Analysis and Modeling

### Descriptive Analysis
- Summary statistics (mean, median, std) for variables like Order Value and Profit.

### Inferential Analysis
- **Correlation Analysis**: Between Delivery Fee and Profit.
- **A/B Testing**: T-tests comparing profit across payment methods.

### Visualization Analysis
- Pie charts for cost and payment method distributions.
- Histograms and boxplots for profit distribution.
- Line charts for trends in orders, fees, and values.
- Bar charts comparing profits across payment methods.

### Predictive Modeling
- **Linear Regression**
- **Random Forest Regressor**
- **K-Nearest Neighbors (KNN)**
- **Logistic Regression** (for classification tasks)

### Model Evaluation
- **R-squared (R²)**: Variance explained.
- **Root Mean Squared Error (RMSE)**: Average prediction error.
- **Bootstrapping**: Confidence intervals for model accuracy.

## Results and Insights
- **Positive Correlation**: Higher delivery fees increase profitability.
- **A/B Testing**: Credit Card payments yield higher profits than Cash on Delivery.
- **Descriptive Findings**: Avg profit ≈ $950 per order.
- **Model Performance**: Random Forest performed best with high R² and low RMSE.

## Implications

### Business Strategy
- Optimize delivery fee pricing.
- Incentivize Credit Card usage.
- Design data-driven promotional offers.

### Decision-Making
- Monitor cost drivers like delivery duration and discounts.
- Implement dynamic pricing based on key order attributes.

## Limitations
- Missing/incomplete data (especially in Discounts column).
- Bootstrapping assumes sample represents entire population.
- A/B test included limited payment types.

## Future Directions
- Add predictors: customer demographics, ratings, etc.
- Explore classification models (profitable vs. unprofitable).
- Use advanced machine learning techniques (e.g., neural networks).

## Files in this Repository
- `food_delivery.csv`: Cleaned dataset.
- `food_orders_new_delhi (1).csv`: Raw dataset.
- `case study original.docx`: Case study report.
- `case_study_ds.ipynb`: Jupyter Notebook with code and analysis.
- `food_delivery_sales_dashboard.pdf`: Summary dashboard.

## Installation and Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/Food-Delivery-Profitability-Analysis-and-Predictive-Modeling.git
    cd Food-Delivery-Profitability-Analysis-and-Predictive-Modeling
    ```

2. Create a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. Install dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn jupyter
    ```

4. Launch Jupyter Notebook:
    ```bash
    jupyter notebook case_study_ds.ipynb
    ```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for improvements or features.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
