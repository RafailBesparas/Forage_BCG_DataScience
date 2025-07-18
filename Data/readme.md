# 📁 Dataset Description
- The dataset consists of three CSV files capturing client characteristics, pricing context, and a preprocessed version for modeling.

- client_data.csv: Contains customer attributes and financial information.
- price_data.csv: Contains product or market price-related data.
- clean_data_after_eda.csv: Merged and cleaned dataset after exploratory data analysis (EDA), ready for modeling.

# client_data.csv – Client Demographics & Financial Data
| Column Name                                                 | Description                                          |
| ----------------------------------------------------------- | ---------------------------------------------------- |
| `client_id`                                                 | Unique identifier for each client                    |
| `age`                                                       | Client’s age in years                                |
| `job`                                                       | Occupation category (e.g., admin, blue-collar)       |
| `marital_status`                                            | Marital status (e.g., single, married, divorced)     |
| `education`                                                 | Education level (e.g., primary, secondary, tertiary) |
| `default`                                                   | Whether the client has credit default (yes/no)       |
| `balance`                                                   | Current account balance                              |
| `housing`                                                   | Whether client has a housing loan                    |
| `loan`                                                      | Whether client has a personal loan                   |
| `contact`                                                   | Type of contact communication                        |
| `day`, `month`, `duration`, `campaign`, `pdays`, `previous` | Campaign details (calls, recency, etc.)              |
| `y`                                                         | Target variable – e.g., subscribed to an offer       |

💰 price_data.csv – Product or Market Context
| Column Name    | Description                                         |
| -------------- | --------------------------------------------------- |
| `price_id`     | Unique identifier for the price record              |
| `client_id`    | Foreign key referencing a client                    |
| `product_type` | Category of the product or financial instrument     |
| `base_price`   | Original market price                               |
| `discount`     | Discount applied (if any)                           |
| `final_price`  | Final price paid after discount                     |
| `price_date`   | Date the price was recorded or transaction occurred |

# 🧼 clean_data_after_eda.csv – Final Processed Dataset
This is the result of EDA and feature engineering. It includes:
1. Cleaned and transformed features
2. Engineered variables like ratios, indicators, or binarized categories
3. Encoded categorical data and scaled numerical features
4. No missing values
- Used as the input for modeling pipelines.

