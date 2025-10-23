# Pension Forecast Calculator

This is a single-file web application designed to help you forecast your pension pot's growth, model retirement income, and stress-test your financial plan using Monte Carlo simulations.

It moves beyond simple calculators by modeling market volatility and inflation, giving you a probabilistic view of your financial future.

Vibe coded using Gemini. N.B I am not a financial advisor.

## Key Features

* **Core Inputs:** Set your current age, desired retirement age, initial investment, and default monthly contributions.

* **State Pension:** Optionally include your state pension, specifying the annual amount and the age you'll start receiving it.

* **Detailed Yearly Plan:** A powerful table that allows you to override the defaults and set custom contribution or withdrawal amounts for every single year of the plan.

* **Monte Carlo Simulation:**

  * Run 1,000 simulations to model a range of possible outcomes instead of a single, fixed return.

  * Set the **Mean Annual Return** (your expected average) and **Return Standard Deviation** (market volatility).

  * Model **Average Inflation** and **Inflation Standard Deviation** to simulate the rising cost of living.

* **Inflation-Adjusted Withdrawals:** Automatically increase your planned withdrawals to keep pace with the simulated inflation, testing your plan's true purchasing power.

* **Dynamic Probability Graph:**

  * **Single Run Mode:** Shows a single, deterministic forecast line.

  * **Monte Carlo Mode:** Displays your forecast as a probability band:

    * **50th Percentile (Median):** The "middle" or most likely outcome (solid black line).

    * **10th-90th Percentile Band:** The shaded blue area representing the range of 80% of all simulated outcomes. The bottom (10th) is a "poor" outcome, and the top (90th) is a "good" outcome.

* **Key Success Metrics:**

  * **Pot at Retirement:** The value of your pot when you retire.

  * **Plan Success Rate:** (Monte Carlo only) The percentage of the 1,000 simulations where your money lasted until age 100.

  * **Runs Out Age:** The age your money runs out.

## How to Use

1. **Welcome Tutorial:** When you first load the app, a tutorial will guide you through the main sections.

2. **Set Your Details:** Use the sliders to set your "Current Age" and "Retirement Age".

3. **Set Default Assumptions:** Input your "Initial Investment," "Default Contribution," "Default Annual Return," and "Default Withdrawal."

4. **Enable Monte Carlo (Recommended):**

   * Check the "Monte Carlo Simulation" box.

   * Set the parameters for return volatility (Std Deviation) and inflation.

   * Check "Adjust withdrawals for inflation" for the most realistic plan.

5. **Customize Your Plan:**

   * Go to the "Customize Yearly Plan" table at the bottom.

   * You can enter a specific monthly contribution for any year *before* retirement.

   * You can enter a specific annual withdrawal for any year *during* retirement.

   * The chart and stats will update instantly with every change.

6. **Analyze the Results:**

   * Look at the "Plan Success Rate" to see how robust your plan is.

   * Check the "10th Percentile" line (bottom of the blue band) to see how your plan holds up in a poor sequence of market returns.

   * Adjust your contributions, retirement age, or withdrawals to see how you can improve your success rate.

## Technology

* **HTML5**

* **Tailwind CSS** (loaded via CDN)

* **Chart.js** (loaded via CDN)

* All logic is contained in a single `pension_forecast.html` file with vanilla JavaScript.
