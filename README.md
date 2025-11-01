# Financial Analysis Toolkit

A lightweight, web-based toolkit for analyzing financial data, generating insights, and visualizing key metrics from company, stock, or personal finance datasets. Built with vanilla JavaScript and runs entirely in the browser—no server required, no data leaves your device.

![Financial Analysis Toolkit](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 🚀 Features

- **Summary Statistics**: Calculate mean, median, standard deviation, min, and max for all numeric columns
- **Year-over-Year Growth**: Analyze percentage growth across time periods
- **Moving Averages**: Compute and visualize moving averages with customizable window sizes
- **Key Financial Ratios**: Automatically calculate common ratios (Current Ratio, Quick Ratio, Debt/Equity, Net Margin)
- **Custom Column Analysis**: Deep-dive into specific metrics with visualization
- **Interactive Visualizations**: SVG-based line charts with tooltips
- **Privacy-First**: All processing happens client-side—your data never leaves your browser

## 📋 Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- CSV file with financial data

## 🎯 Quick Start

### Option 1: Use GitHub Pages (Recommended)

1. Visit the live demo: `https://yourusername.github.io/financial-analysis-toolkit/`
2. Upload your CSV file
3. Select analysis type and explore insights

### Option 2: Run Locally

1. Clone the repository:
```bash
git clone https://github.com/yourusername/financial-analysis-toolkit.git
cd financial-analysis-toolkit
```

2. Open `index.html` in your browser:
```bash
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

That's it! No build process, no dependencies to install.

## 📊 CSV File Format

Your CSV file should have:
- **Header row** with column names
- **Numeric columns** for analysis (revenue, expenses, assets, etc.)
- **Optional date/year column** for time-series analysis

### Example CSV Structure:

```csv
Year,Revenue,Net Income,Total Assets,Current Assets,Current Liabilities,Total Debt,Total Equity
2021,1000000,150000,2500000,800000,300000,500000,1800000
2022,1200000,180000,2800000,900000,350000,550000,2000000
2023,1500000,225000,3200000,1100000,400000,600000,2300000
```

### Supported Column Names for Ratios:

For automatic ratio calculations, use these column names (case-insensitive):
- `Current Assets`, `Current Liabilities` → Current Ratio
- `Inventories` → Quick Ratio (requires Current Assets & Liabilities)
- `Total Debt`, `Total Equity` → Debt/Equity Ratio
- `Net Income`, `Revenue` → Net Margin

## 🛠️ Usage Guide

### 1. Upload Data
- Click "Choose File" and select your CSV file
- The toolkit will automatically detect numeric columns

### 2. Select Analysis Type

#### Summary Statistics
Provides comprehensive statistical overview of all numeric columns:
- Mean, Median, Standard Deviation
- Minimum and Maximum values

#### Year-over-Year Growth
Calculates percentage change between consecutive rows:
- Assumes row order represents time progression
- Works best with annual or quarterly data

#### Moving Average
Smooth out fluctuations in your data:
- Select target column
- Choose window size (number of periods to average)
- View original data vs. moving average chart

#### Key Financial Ratios
Automatically calculates standard financial metrics:
- Current Ratio (liquidity)
- Quick Ratio (liquidity without inventory)
- Debt/Equity Ratio (leverage)
- Net Margin (profitability)

#### Custom Column Analysis
Focus on a specific metric:
- Select any numeric column
- Get summary statistics
- View visualization

### 3. Analyze & Export
- Click "Analyze" to generate results
- Take screenshots of visualizations
- Copy table data as needed

## 🏗️ Project Structure

```
financial-analysis-toolkit/
├── index.html          # Main application file (self-contained)
├── README.md           # This file
├── LICENSE             # MIT License
└── examples/           # Sample CSV files
    ├── company-financials.csv
    ├── stock-prices.csv
    └── personal-budget.csv
```

## 🎨 Customization

The toolkit uses CSS custom properties for easy theming. Edit these variables in `index.html`:

```css
:root {
    --color-primary: #21808D;        /* Primary brand color */
    --color-background: #FCFCF9;     /* Page background */
    --color-surface: #FFFFFD;        /* Card background */
    --color-text: #13343B;           /* Text color */
    /* ... more variables ... */
}
```

## 🔒 Privacy & Security

- **No Server Communication**: All data processing happens in your browser
- **No Data Storage**: Files are processed in memory only
- **No Tracking**: No analytics or telemetry
- **Open Source**: Full transparency—inspect the code yourself

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Ideas for Contributions:
- Additional analysis types (correlation, regression, forecasting)
- More chart types (bar charts, scatter plots)
- Export functionality (CSV, PDF, PNG)
- Data validation and error handling improvements
- Additional financial ratios
- Dark mode support
- Mobile responsiveness enhancements

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Known Issues

- Large CSV files (>5MB) may cause performance issues in some browsers
- Chart rendering is optimized for datasets with <1000 data points
- Internet Explorer is not supported

## 📚 Technologies Used

- **HTML5** - Structure and semantics
- **CSS3** - Styling and responsive design
- **Vanilla JavaScript (ES6+)** - Application logic
- **PapaParse** - CSV parsing library
- **SVG** - Data visualization

## 🙏 Acknowledgments

- [PapaParse](https://www.papaparse.com/) for excellent CSV parsing
- Design inspired by modern fintech applications

## 📧 Contact

Questions or suggestions? Open an issue on GitHub!

---

**Made with ❤️ for financial analysis enthusiasts**
