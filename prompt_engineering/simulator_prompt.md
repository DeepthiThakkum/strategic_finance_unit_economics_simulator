You are a Principal Strategic Finance Engineer and expert frontend developer. 

Build a complete, production-grade, single-file HTML/JavaScript web application called "StratFin: Dynamic Unit Economics & Payback Simulator". 

The entire app must run self-contained in a single index.html file using Tailwind CSS (via CDN) for styling and Chart.js (via CDN) for data visualizations.

---

### 1. Functional Requirements & Core Formulas

The simulator must dynamically calculate and display:

1. **Customer Lifetime Value (LTV):**
   - Annual Contract Value (ACV) = Average deal size ($).
   - Gross Margin % (COGS subtracted).
   - Annual Churn Rate % (Logo or Gross Revenue Churn).
   - Formula: `LTV = (ACV * Gross Margin %) / Churn Rate %`
   - Also allow factoring in Net Revenue Retention (NRR %) for a dynamic compounding LTV.

2. **CAC Payback Period (Months):**
   - Blended Customer Acquisition Cost (CAC) ($).
   - Monthly Gross Profit = `(ACV / 12) * Gross Margin %`
   - Payback Formula: `CAC Payback (Months) = CAC / Monthly Gross Profit`
   - Categorize output: Excellent (< 12 mo), Good (12–18 mo), Concerning (18–24 mo), Danger (> 24 mo).

3. **LTV:CAC Ratio:**
   - Formula: `LTV / CAC`
   - Benchmark badge: Under-investing (> 5x), Healthy (3x–5x), Fragile (1.5x–3x), Value Destructive (< 1.5x).

4. **SaaS Magic Number & Burn Multiple:**
   - Input: Net New ARR added in quarter vs. Previous Quarter Sales & Marketing (S&M) expense.
   - Formula: `Magic Number = (Quarterly Net New ARR * 4) / Prior Quarter S&M`

5. **Cash-Trough & Cumulative Cash Flow Curve (0 to 36 Months):**
   - Plot cumulative net cash flow per customer vintage over a 36-month timeline.
   - Support two payment terms toggle:
     * **Monthly in Advance:** Month 0 cash outflow is `-CAC`. Customer pays `(ACV / 12)` each month minus monthly COGS. Cash recovery is gradual.
     * **Annual Upfront:** Month 0 cash inflow is `+ACV - CAC`. Months 1–11 incur monthly COGS. Month 12 renews with `+ACV * (NRR %)`, etc.
   - Display the **Max Cash Trough ($)** and **Breakeven Month** directly on the chart.

---

### 2. UI/UX Specifications

- **Theme & Layout:** Clean executive financial dashboard. Dark slate or clean modern neutral theme. Responsive 2-column or 3-column grid layout (Inputs Panel on the left, KPI Summary Cards & Charts on the right).
- **Interactive Controls (Sliders + Number Inputs synced):**
  - ACV ($1,000 to $500,000; default $36,000)
  - Blended CAC ($1,000 to $200,000; default $24,000)
  - Gross Margin % (20% to 95%; default 78%)
  - Annual Logo Churn % (2% to 40%; default 10%)
  - Net Expansion / NRR % (80% to 150%; default 115%)
  - Billing Term: Toggle between "Annual Upfront" and "Monthly in Advance"
- **Executive KPI Cards:**
  - LTV ($), CAC Payback (Months), LTV:CAC, Magic Number, and Max Cash Deficit per Customer. Include color-coded status badges.
- **Chart.js Visualization:**
  - Line chart showing 36-month Cumulative Cash Flow ($).
  - Include a zero-line marker (`$0 Breakeven`).
  - Tooltips formatted cleanly as currency ($) and months.
- **Strategic Finance Takeaway Box:**
  - A dynamic, rule-based text summary that synthesizes the metrics into executive talking points (e.g., "At a 14.8 month payback with annual upfront billing, working capital remains net positive despite high CAC...").

---

### 3. Deliverable Instructions
- Output valid, clean, and complete HTML within a single code block. 
- Include all necessary `<script>` tags for Tailwind CSS and Chart.js.
- Ensure all input state changes recalculate and update the Chart.js instance seamlessly without page reloads.