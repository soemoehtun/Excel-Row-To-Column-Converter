
# Excel Row-to-Column Conversion Tool

A web-based tool that transforms data from wide format to long format by unpivoting selected columns. Perfect for preparing data for BI tools, dashboards, and analytics applications.

## 🌟 Features

- **File Upload**: Supports CSV files with automatic header detection
- **Flexible Column Selection**: Choose which columns to keep and which to pivot
- **Client-Side Processing**: All transformations happen in your browser - no data leaves your device
- **Excel Export**: Download results directly as Excel files
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **User-Friendly Interface**: Intuitive tabbed interface with built-in guide
- **Live Examples**: Includes sample data and transformation examples

## 🚀 Quick Start

### Option 1: Use Live Version
Visit the [live demo](https://soemoehtun.github.io/profolio/) to use the tool immediately.

### Option 2: Local Setup
1. Clone or download this repository
2. Open `index.html` in your web browser
3. Start converting your data!

## 📖 How to Use

### Step 1: Upload Your Data
- Click "Choose File" and select your CSV file
- Click "Import Data" to load the file
- The tool will display all available columns

### Step 2: Select Columns
- **Columns to Keep**: Select identifier columns (Site, Date, Country, etc.)
- **Columns to Pivot**: Select value columns (KPIs, metrics, etc.)
- Use the quick selection buttons for bulk operations

### Step 3: Configure Options
- Toggle "Include Pivot Column Name" to add a column with original field names
- This is useful for tracking which metric each value represents

### Step 4: Run Conversion
- Click "Run Conversion & Download"
- The tool will process your data and automatically download the Excel file

## 📊 Example Transformation

**Input (Wide Format):**
```
Site,Date,KPI1,KPI2
A,2025-01-01,10,20
A,2025-01-02,15,25
B,2025-01-01,5,8
```

**Output (Long Format):**
```
Site,Date,KPI Name,KPI Value
A,2025-01-01,KPI1,10
A,2025-01-01,KPI2,20
A,2025-01-02,KPI1,15
A,2025-01-02,KPI2,25
B,2025-01-01,KPI1,5
B,2025-01-01,KPI2,8
```

## 🛠️ Technical Details

### Dependencies
- **Tailwind CSS**: For responsive styling (loaded via CDN)
- **Papa Parse**: For CSV parsing (loaded via CDN)
- **SheetJS (xlsx)**: For Excel file generation (loaded via CDN)

### Browser Compatibility
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

### File Requirements
- **Input**: CSV files with header row
- **Output**: Excel (.xlsx) files
- **Max Size**: Limited by browser memory (typically works well with files up to 10MB)

## 🎯 Use Cases

This tool is ideal when you need to:
- Prepare data for Power BI, Tableau, or other BI tools
- Convert survey results from wide to long format
- Transform time-series KPI data for analysis
- Normalize data for database imports
- Create flexible datasets for dashboarding

### Styling
Modify the appearance by adjusting Tailwind classes in the HTML file or adding custom CSS rules.

### Processing Logic
The core transformation logic is in the `btnRun` event listener. Modify this section to change how data is processed.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

Created with ❤️ by [Soe Moe Tun](https://soemoehtun.github.io/profolio/)

## 🆘 Support

If you encounter any issues or have questions:
1. Check the built-in User Guidelines tab in the application
2. Review the examples provided
3. Create an issue in the repository

---

**Note**: This tool processes all data locally in your browser. No data is transmitted to any server, ensuring your information remains private and secure.
