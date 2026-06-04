# Personal Finance Dashboard

A modern, fully-featured personal finance dashboard built with React, TypeScript, and Recharts. Track expenses, visualize spending patterns, and manage budgets with an intuitive interface.

## Features

✨ **Core Features**
- 📤 **CSV Upload with Drag-and-Drop** - Upload transaction data easily with PapaParse
- 🤖 **Auto-Categorization** - Automatically categorizes transactions into 8 categories using keyword matching:
  - Food
  - Transport
  - Housing
  - Shopping
  - Health
  - Entertainment
  - Travel
  - Other

- 📊 **Interactive Charts** - Three switchable chart types powered by Recharts:
  - Donut Pie Chart - Category spending breakdown
  - Horizontal Bar Chart - Category comparison
  - Monthly Line Chart - Spending trends over time

- 💰 **Summary Metrics** - Four metric cards displaying:
  - Total spent for the month
  - Transaction count
  - Average spend per transaction
  - Number of categories used

- 🎯 **Budget Alerts** - Progress bars for each category with color coding:
  - Green for on-track spending
  - Yellow for approaching budget limits (80%+)
  - Red when over budget

- 📋 **Transaction Table** - Scrollable table with:
  - Colored category badges
  - Date and description
  - Amount formatting
  - Sorted by date (newest first)

- 🌓 **Dark/Light Mode** - Toggle between themes with CSS variables
- 📅 **Month Filter** - Select and view data for different months
- 💾 **Pre-loaded Sample Data** - Dashboard works immediately on first render

## Installation

### Prerequisites
- Node.js 18+ and npm

### Setup

1. **Clone or navigate to the project folder**
   ```bash
   cd "personal finance dashboard"
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

The application will open in your browser at `http://localhost:3000`

## Usage

### Uploading CSV Data

1. **Prepare your CSV file** with the following columns:
   ```csv
   date,description,amount
   2024-01-15,Coffee at Starbucks,6.50
   2024-01-15,Gas Station,65.00
   2024-01-16,Monthly Rent,1500.00
   ```

2. **Upload** by either:
   - Dragging and dropping the CSV file onto the upload zone
   - Clicking the upload zone and selecting a file

3. **Transactions are automatically categorized** based on keywords in the description

### Using the Dashboard

- **Filter by Month** - Use the month dropdown to view different time periods
- **View Charts** - Switch between pie, bar, and line chart tabs to visualize spending
- **Monitor Budget** - Check budget alerts to see which categories are at risk
- **Review Transactions** - Scroll through the transaction table to see details
- **Toggle Theme** - Click the sun/moon button in the header to switch between light and dark modes

## CSV Format

The application expects CSV files with at least these three columns:

| Column | Format | Example |
|--------|--------|---------|
| date | YYYY-MM-DD | 2024-01-15 |
| description | Text | Coffee at Starbucks |
| amount | Number | 6.50 |

Column names are case-insensitive. The application will automatically categorize transactions based on keywords in the description.

## Building for Production

```bash
npm run build
```

The built application will be in the `dist` folder.

## Technologies Used

- **React 18** - UI library
- **TypeScript** - Type safety
- **Vite** - Fast build tool
- **Recharts** - Interactive charts
- **PapaParse** - CSV parsing
- **CSS Variables** - Theme support

## Project Structure

```
src/
├── components/          # React components
│   ├── MetricCard.tsx
│   ├── CSVUpload.tsx
│   ├── Charts.tsx
│   ├── TransactionTable.tsx
│   ├── BudgetAlert.tsx
│   ├── Header.tsx
│   └── index.ts
├── types.ts            # TypeScript types
├── utils.ts            # Utility functions
├── sampleData.ts       # Sample transactions and budgets
├── App.tsx             # Main app component
├── App.css             # App styles
├── index.css           # Global styles
└── main.tsx            # Entry point
```

## Features Details

### Auto-Categorization Logic

The app uses keyword matching to automatically categorize transactions:

- **Food** - restaurant, cafe, pizza, burger, grocery, supermarket, etc.
- **Transport** - gas, taxi, uber, metro, bus, train, airline, etc.
- **Housing** - rent, mortgage, utilities, electricity, water, internet, etc.
- **Shopping** - mall, store, amazon, clothing, shoes, retail, etc.
- **Health** - doctor, hospital, pharmacy, medicine, dental, gym, etc.
- **Entertainment** - movie, cinema, music, concert, game, spotify, netflix, etc.
- **Travel** - hotel, airbnb, vacation, trip, resort, accommodation, etc.
- **Other** - Default category if no match found

### Budget Alerts

Each category has a default budget:
- Food: $400
- Transport: $200
- Housing: $1,800
- Shopping: $300
- Health: $150
- Entertainment: $150
- Travel: $500
- Other: $100

The progress bars show:
- **Green** - 0-79% of budget used
- **Yellow** - 80-99% of budget used
- **Red** - 100%+ of budget used

### Currency Formatting

All currency values are automatically formatted to 2 decimal places using the en-US locale.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For issues or questions, please create an issue in the repository.

---

**Enjoy tracking your finances! 💳✨**
