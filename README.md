# Advanced Pension Forecast Calculator

This is a single-file web application designed to help you forecast your pension pot's growth, model retirement income, and stress-test your financial plan using a professional-grade Monte Carlo simulation engine.

It moves beyond simple calculators by modeling your portfolio as a sophisticated mix of assets and accounting for realistic market volatility, inflation, and fees. This gives you a probabilistic view of your financial future.

Provided without warranty. I am neither a statistician or a fincial planner.

Created with help from Gemini AI.

## Key Features

* **Core Inputs:** Set your current age, desired retirement age, initial investment, and default monthly contributions.

* **State Pension:** Optionally include your state pension, specifying the annual amount and the age you'll start receiving it.

* **Detailed Yearly Plan:** A powerful table that allows you to override the defaults and set custom contribution or withdrawal amounts for every single year of the plan.

### Advanced Monte Carlo Simulation

This is the core of the calculator. Instead of assuming a fixed return (e.g., "7% every year"), the app runs 1,000 unique simulations to model a range of possible outcomes.

* **Asset Allocation (Stocks vs. Bonds):**

  * Your portfolio is modeled as a mix of Stocks (Equities) and Bonds (Fixed Income). You can set your desired allocation (e.g., 60% Stocks / 40% Bonds) with a simple slider.

  * **Advanced Asset Assumptions:** A hidden section allows you to define the **mean (average) return**, **standard deviation (volatility)**, and **correlation** for both asset classes, giving you full control over the model.

* **Annual Investment Fees:**

  * A crucial input for realism. This slider lets you set an annual fee (e.g., 0.5%) that is subtracted from your returns *every year*, demonstrating the long-term impact of costs on your portfolio.

* **Inflation Modeling:**

  * The simulation models inflation as its own volatile variable. You can set the **Average Annual Inflation** and its **Volatility (Std Dev)**.

  * **"Adjust withdrawals for inflation"**: This critical feature, when checked, will automatically increase your planned withdrawals each year to keep pace with the *simulated* inflation, testing your plan's true purchasing power.

* **Lognormal Statistical Model:**

  * The simulation "engine" uses a **Lognormal Distribution**, which is the financial industry standard. This is more realistic than a simple bell curve ("Normal" distribution) as it prevents impossible outcomes (like losing more than 100% of your money) and more accurately models the "fatter tails" (extreme crashes or booms) of real markets.

### How to Read the Results

* **Probability Graph:** When Monte Carlo is on, the graph shows a **probability band**:

  * **50th Percentile (Solid Black Line):** The "median" or most likely outcome. 50% of simulations did better, 50% did worse.

  * **10th-90th Percentile (Blue Band):** This shaded area represents the "range of most likely outcomes." 80% of all simulations fell within this band.

  * **10th Percentile (Bottom Line):** This is your "stress test" or "poor outcome" line. There is a 1-in-10 chance your result will be this bad or worse.

* **Key Success Metrics:**

  * **Median Pot at Retirement:** The 50th percentile value of your pot when you retire.

  * **Plan Success Rate:** The single most important number. This shows the percentage of the 1,000 simulations where your money lasted until age 100.

  * **Median Runs Out Age:** In the simulations that *did* fail, this is the median age at which the money ran out.

## Technology

* **HTML5**

* **Tailwind CSS** (loaded via CDN)

* **Chart.js** (loaded via CDN)

* All logic is contained in a single `.html` file with vanilla JavaScript.
