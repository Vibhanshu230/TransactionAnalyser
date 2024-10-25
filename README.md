# TransactionAnalyzer

## Description
TransactionAnalyzer is a Python-based project designed to analyze and derive insights from financial transaction data across multiple accounts. It processes data through multiple stages, including generation, preprocessing, feature extraction, and visualization. TransactionAnalyzer helps identify key patterns in financial behavior, making it useful for both personal finance tracking and financial data analysis in organizations.

## Features

### 1. Data Generation
   - **Description**: Generates synthetic financial transaction data, including transaction type, account number, amount, balance, date, and transaction channel.
   - **Application**: Simulates real-world transaction data for testing financial analysis methods without exposing sensitive data from actual users.

### 2. Data Preprocessing
   - # Filling Missing Values 
     - **Description**: Fills any missing values in the `amount` column with the median transaction amount.
     - **Application**: Handling missing data is crucial in financial datasets to ensure analyses are not skewed due to gaps. Filling with the median helps maintain data integrity without introducing outliers.
   
   - # Dropping Duplicates  
     - **Description**: Removes duplicate rows to maintain the uniqueness of each transaction record.
     - **Application**: Duplicate transactions can distort spending patterns, potentially leading to inaccurate analyses or suspicions of fraud. Removing duplicates ensures data reliability.

### 3. Encoding Transaction Channels
   - **One-Hot Encoding**  
     - **Description**: Converts categorical values in the `transaction_channel` column into binary columns.
     - **Application**: In machine learning, categorical data must be numerical. This encoding allows for easy model integration, helping banks or fintech companies analyze transaction behavior by channel (e.g., UPI vs. net banking).

### 4. Outlier Detection in Balance Data
   - **Description**: Identifies outliers in account balance values using the interquartile range (IQR) method.
   - **Application**: Detecting balance outliers helps in fraud detection and financial health monitoring. For instance, a sudden spike or drop in balance might indicate suspicious activity or highlight financial stress.

### 5. Transaction Date Extraction
   - **Extracting Important Transaction Dates**  
     - **Description**: Retrieves the dates of the highest credit transaction and the lowest debit transaction.
     - **Application**: Tracking significant transactions is crucial for understanding financial events, such as salary credits or large expenditures, and helps users and analysts better manage finances.

### 6. Feature Engineering
   - **Average and Maximum Balances Over Different Periods**  
     - **Description**: Derives features such as average and maximum balances over 7, 15, and 30-day periods for each account.
     - **Application**: These insights provide an understanding of short- and medium-term financial patterns, useful in budgeting, credit risk assessment, and financial planning.
   
   - **Total Average Balance Over Different Periods**  
     - **Description**: Computes the total average balance across all accounts for 7, 15, and 30-day periods.
     - **Application**: Offers a consolidated view of financial health across accounts, helping users monitor liquidity and savings across different time frames.

### 7. Data Visualization
   - **Plotting Average and Maximum Balances for Accounts**  
     - **Description**: Visualizes average and maximum balances across accounts over the past 7, 15, and 30 days using line plots.
     - **Application**: Visual trends of balances help in spotting financial stability or volatility, assisting both personal users and analysts in making informed decisions.

   - **Total Average Balance Plot**  
     - **Description**: Plots total average balance over different time periods to show aggregate financial trends.
     - **Application**: Provides a broad perspective on overall account health, which is useful for budgeting and understanding cash flow trends.
     - 
## Tech Stack
- **Python**: A core programming language for the project.
- **Pandas**: Data handling and manipulation.
- **Numpy**: Numerical operations.
- **Scikit-Learn**: One-hot encoding for categorical data.
- **Seaborn & Matplotlib**: Data visualization for transaction and balance trends.
