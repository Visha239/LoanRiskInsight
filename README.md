# LoanRiskInsight
LoanRiskInsight is a project designed to analyze and classify loan risk using borrower data. This project leverages Python, pandas, and seaborn to derive insights from the dataset and make informed recommendations on borrower risk and communication strategies.

## Project Structure

- **data/**: Contains the dataset file.
- **notebooks/**: Contains the Jupyter notebook used for data analysis.
- **README.md**: Project documentation.
- **requirements.txt**: List of dependencies.
- **LICENSE**: License for the project.
- **.gitignore**: Specifies files and directories to be ignored by git.

## Dataset

The dataset contains loan data for various borrowers in a loan portfolio. The columns are:

- `Amount Pending`: EMI amount pending.
- `State`: The borrower's state.
- `Tenure`: Total tenure of the loan.
- `Interest Rate`: Interest rate of the loan.
- `City`: The city of the borrower.
- `Bounce String`: Indicates the borrower’s payment behavior.
- `Disbursed Amount`: Total disbursed amount of the loan.
- `Loan Number`: Unique identifier for the loan.

## Analysis

### Risk Labeling

Borrowers are labeled based on their bounce behavior:
- **Low Risk**: No bounce in the last 6 months.
- **Medium Risk**: Max two bounces in the last 6 months, not in the last month.
- **High Risk**: All other cases.
- **Unknown Risk**: New customers (FEMI).

### Tenure Labeling

- **Early Tenure**: On book for 3 months.
- **Late Tenure**: 3 months away from closing.
- **Mid Tenure**: Everyone else.

### Ticket Size Segmentation

Borrowers are segmented based on the sum of `Amount Pending`:
- **Low Ticket Size**
- **Medium Ticket Size**
- **High Ticket Size**
- 

### Channel Spend Recommendations

Communication channels to reduce bounce:
- **Whatsapp Bot**: Low cost, effective for good repayment behavior and low EMIs.
- **Voice Bot**: Mid-cost, effective for borrowers from metropolitan areas and low-interest rates.
- **Human Calling**: High cost, used when necessary.
  
- ## Usage

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/LoanRiskInsight.git
    ```

2. Navigate to the project directory:
    ```sh
    cd LoanRiskInsight
    ```

3. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Open the Jupyter notebook:
    ```sh
    jupyter notebook notebooks/LoanRiskAnalysis.ipynb
    ```

## Results

The project provides visualizations and insights into the distribution of borrowers based on risk, tenure, and ticket size. It also recommends communication channels to optimize spend and improve repayment rates.

##Requirments
pandas
numpy
matplotlib
seaborn
jupyter
