# Blue Market Strategy Simulator

An educational Next.js app for exploring the Blue detergent market strategy case. Designed for deployment on Vercel.

## What it includes

- Case overview with historical Blue financials and 2018 market shares
- Competitor research and formulation facts from the supplied case pre-read
- Strategy controls for price, marketing budget, channel allocation, formulation mix, and target segment
- Transparent illustrative market-response model
- Simulated revenue, costs, profit, and market-share comparisons
- Saved scenarios in browser local storage
- CSV export of simulation results
- Editable sensitivity assumptions

## Important model note

The PDF provides case background and historical data, but not the proprietary simulation's full market-response equations. The app therefore uses a simplified, illustrative model. Historical facts and assumptions are explicitly separated in the UI. It is not a reproduction of Harvard Business Publishing's proprietary simulation and should not be treated as a real-world forecast.

## Run locally

Requirements: Node.js 20+ and npm.

```bash
npm install
npm run dev
```

Open http://localhost:3000.

To verify a production build:

```bash
npm run build
npm start
```

## Deploy to Vercel

### Option A: GitHub (recommended)
1. Create a new empty repository on GitHub.
2. Upload/extract these project files into the repository and commit them.
3. In Vercel, choose **Add New → Project** and import the repository.
4. Keep the detected framework as Next.js.
5. Click **Deploy**. No environment variables or database are required for the first version.

### Option B: Vercel CLI
1. Install Node.js 20+.
2. Extract the ZIP and open a terminal in the project folder.
3. Run `npm install`.
4. Install the CLI with `npm install -g vercel`.
5. Run `vercel` and follow the prompts; run `vercel --prod` when ready for production.

## Data and persistence

No external market-data API is used. Scenario history is saved in the current browser's `localStorage`; it is not shared between devices or users. Database-backed accounts and shared scenario history can be added later.

## Case figures preloaded

- Blue 2018 revenue: $225.3M
- Blue 2018 variable costs: $67.6M
- Blue 2018 fixed costs: $87.0M
- Blue 2018 other costs: $32.9M
- Blue 2018 operating profit: $37.8M
- Market share: Blue 11.0%, Turbo 44.1%, Fresh 26.3%, Store brands 18.6%
- Channel price per 100 units: Blue $7, Turbo $10, Fresh $8, Store brands $6

All figures above are from the case pre-read. The $15M marketing calibration and market-response coefficients are illustrative assumptions, not case facts.
