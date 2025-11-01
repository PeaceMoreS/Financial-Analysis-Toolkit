# Quick Start Guide - Financial Analysis Toolkit

## 🎯 Getting Started in 3 Steps

### Step 1: Set Up Your Repository

```bash
# Create a new repository on GitHub first, then:
git clone https://github.com/yourusername/financial-analysis-toolkit.git
cd financial-analysis-toolkit

# Add the files
git add .
git commit -m "Initial commit: Financial Analysis Toolkit"
git push origin main
```

### Step 2: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll to **Pages** section (left sidebar)
4. Under "Source", select **main** branch
5. Click **Save**
6. Your site will be live at: `https://yourusername.github.io/financial-analysis-toolkit/`

### Step 3: Test It Out

Visit your live site and test with sample data!

## 📁 Example CSV Files

### Sample 1: Company Financials

Create `examples/company-financials.csv`:

```csv
Year,Revenue,Net Income,Total Assets,Current Assets,Current Liabilities,Total Debt,Total Equity,Inventories
2020,950000,120000,2200000,700000,280000,450000,1650000,150000
2021,1000000,150000,2500000,800000,300000,500000,1800000,180000
2022,1200000,180000,2800000,900000,350000,550000,2000000,200000
2023,1500000,225000,3200000,1100000,400000,600000,2300000,250000
```

### Sample 2: Stock Prices

Create `examples/stock-prices.csv`:

```csv
Date,Open,High,Low,Close,Volume
2024-01-01,150.25,152.80,149.50,151.75,5000000
2024-01-02,151.80,153.25,150.90,152.50,4800000
2024-01-03,152.60,154.10,151.80,153.90,5200000
2024-01-04,154.00,155.50,153.20,154.80,5500000
2024-01-05,154.90,156.80,154.00,156.25,6000000
```

### Sample 3: Personal Budget

Create `examples/personal-budget.csv`:

```csv
Month,Income,Expenses,Savings,Investments
Jan-2024,5000,3200,1800,500
Feb-2024,5000,3400,1600,400
Mar-2024,5200,3300,1900,600
Apr-2024,5000,3500,1500,350
May-2024,5500,3200,2300,800
```

## 🚀 Usage Examples

### Analyze Company Performance

1. Upload `company-financials.csv`
2. Select **"Year-over-Year Growth"**
3. Click **Analyze**
4. See growth trends across all metrics

### Calculate Financial Health

1. Upload `company-financials.csv`
2. Select **"Key Financial Ratios"**
3. Click **Analyze**
4. Review liquidity and leverage ratios

### Track Stock Trends

1. Upload `stock-prices.csv`
2. Select **"Moving Average"**
3. Choose "Close" column
4. Set window size to 3
5. Click **Analyze**
6. View smoothed price trend

### Budget Analysis

1. Upload `personal-budget.csv`
2. Select **"Summary Statistics"**
3. Click **Analyze**
4. See average income, expenses, and savings

## 🔧 Customization Tips

### Change Colors

Edit these CSS variables in `index.html`:

```css
:root {
    --color-primary: #21808D;        /* Change to your brand color */
    --color-background: #FCFCF9;     /* Page background */
    --color-surface: #FFFFFD;        /* Card background */
}
```

### Add Your Branding

Replace the `<h1>` text:

```html
<h1>Your Company - Financial Analysis</h1>
```

### Modify Analysis Options

Add new analysis types in the select dropdown:

```html
<select id="analysisType">
    <option value="summary">Summary Statistics</option>
    <option value="growth">Year-over-Year Growth</option>
    <!-- Add your custom analysis here -->
    <option value="myanalysis">My Custom Analysis</option>
</select>
```

## 🐛 Troubleshooting

### CSV Not Loading?
- Ensure first row has headers
- Check for special characters (use UTF-8 encoding)
- Make sure numeric columns contain only numbers

### Ratios Showing Dashes?
- Check column names match exactly (case-insensitive):
  - "Current Assets", "Current Liabilities"
  - "Total Debt", "Total Equity"
  - "Net Income", "Revenue"

### Chart Not Appearing?
- Ensure selected column has numeric values
- Need at least 2 data points for visualization

## 📚 Next Steps

1. ⭐ Star the repository
2. 🍴 Fork it to make your own version
3. 📝 Open issues for bugs or feature requests
4. 🤝 Submit pull requests with improvements

## 💡 Pro Tips

- **Large Datasets**: For files over 1MB, consider filtering data before upload
- **Time Series**: Always use a date/year column for growth analysis
- **Ratios**: Follow standard accounting column names for automatic detection
- **Export**: Use browser print-to-PDF to save reports
- **Backup**: Keep original CSV files—the toolkit doesn't modify them

---

Happy analyzing! 📊
