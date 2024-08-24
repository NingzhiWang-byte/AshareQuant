# Stock Selection and Analysis Tool

## Overview
This project is a comprehensive stock selection and analysis tool designed for the Chinese stock market. It implements various strategies to select stocks based on technical indicators and historical performance, and then analyzes their future performance.

## Features
- Data preprocessing and manipulation using pandas and numpy
- Technical analysis including Moving Averages (MA5, MA10, MA20)
- Volume analysis and change calculation
- Customizable stock selection criteria
- Performance backtesting
- Future performance prediction (up to D+20)

## Requirements
- Python 3.x
- pandas
- numpy
- efinance

## Installation
1. Clone this repository:
   ```
   git clone https://github.com/yourusername/stock-selection-tool.git
   cd stock-selection-tool
   ```

2. Install required packages:
   ```
   pip install pandas numpy efinance
   ```

## Usage
1. Prepare your data:
   - Ensure you have historical stock data in the correct format
   - The script uses `efinance` to fetch real-time data

2. Set your parameters:
   - Adjust the `start_tactic_date` and `end_tactic_date` in the script
   - Modify the selection criteria parameters (e.g., `x1`, `x2`, `a1`, `a2`, `a3`, `a4`)

3. Run the script:
   ```
   python stock_selection_tool.py
   ```

4. Check the output:
   - `portfolio_return.xlsx`: Contains the daily selected stocks and their returns
   - `result_df.xlsx`: Detailed analysis of selected stocks including future performance

## Key Components

### Data Preprocessing
- `get_log_growth`: Calculates logarithmic growth of stock prices
- `get_volume_change`: Calculates volume changes and logarithmic growth
- `get_volatility`: Calculates price volatility
- `get_pillar_height`: Calculates the height of price candlesticks
- `get_line_height`: Calculates the upper shadow of candlesticks

### Stock Selection
The tool selects stocks based on several criteria:
1. MA5 > MA10 > MA20
2. Current price relative to MA5
3. Lowest price relative to MA5
4. Volatility and candlestick patterns
5. Recent price increases

### Performance Analysis
- Calculates returns for various holding periods (D+1 to D+20)
- Computes average portfolio return

## Customization
You can customize the selection criteria by modifying the parameters in the script:
- `x1`, `x2`: Related to volatility and candlestick patterns
- `a1`, `a2`, `a3`: Price levels relative to moving averages
- `a4`: Threshold for recent price increases

## Output
The script generates two Excel files:
1. `portfolio_return.xlsx`: Daily selected stocks and overall portfolio performance
2. `result_df.xlsx`: Detailed analysis of each selected stock, including future performance up to 20 days

## Notes
- This tool is designed for the Chinese stock market and uses Chinese stock codes (starting with 00, 30, 60)
- The script includes handling for Chinese market holidays
- Backtesting is performed from the start date to the end date specified

## Disclaimer
This tool is for educational and research purposes only. It is not financial advice. Always do your own research and consult with a financial advisor before making investment decisions.

## License
[MIT License](LICENSE)

## Contributing
Contributions, issues, and feature requests are welcome. Feel free to check [issues page](https://github.com/yourusername/stock-selection-tool/issues) if you want to contribute.

## Author
[Your Name]

