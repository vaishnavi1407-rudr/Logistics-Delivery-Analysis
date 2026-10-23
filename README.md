Logistics Delivery Performance Analysis
Project Overview
This project explores delivery performance in a logistics scenario using Python. The goal is to identify patterns associated with late deliveries and propose data-driven ways to improve delivery planning, operational efficiency, and cost management.
Dataset note: The CSV used in this project is a simulated practice dataset created for learning and demonstration. The findings should not be treated as evidence about a real logistics company.

Objectives
- Explore delivery records and check data quality.
- Calculate key performance indicators (KPIs) for delivery performance.
- Compare delivery delays across traffic levels, weather conditions, vehicle types, months, and distance categories.
- Create visualizations to communicate findings.
- Outline how predictive analytics and optimization could support logistics decisions.
Repository Structure
Logistics-Delivery-Analysis/
├── data/
│   ├── README.md
│   └── logistics_delivery_data.csv
├── notebook/
│   ├── README.md
│   └── Week1_Logistics_Delivery_Analysis.ipynb
├── report/
│   └── README.md
└── README.md
Dataset Description
The dataset contains 500 rows and 11 columns.
Column	Description
order_id	Unique order identifier
order_date	Date the order was recorded
distance_km	Delivery distance in kilometres
traffic_level	Traffic category: Low, Medium, High, or Unknown after cleaning
weather	Weather category: Clear, Rain, Storm, or Unknown after cleaning
vehicle_type	Vehicle used for the delivery
order_value_inr	Order value in Indian rupees
promised_delivery_minutes	Promised delivery duration in minutes
actual_delivery_minutes	Actual delivery duration in minutes
delivery_cost_inr	Delivery cost in Indian rupees
delivery_status	Whether the delivery was On Time or Delayed


Tools and Libraries
- Python
- Google Colab / Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn (for proposed future predictive modelling)
How to Run
1. Open the notebook notebook/Week1_Logistics_Delivery_Analysis.ipynb in Google Colab.
2. Ensure the CSV file is available. If reading from the Colab session's uploaded files, upload logistics_delivery_data.csv and use:
   import pandas as pd
   df = pd.read_csv('/content/logistics_delivery_data.csv')
3. Run the notebook cells in order.
4. If the CSV is stored elsewhere, update the file path in pd.read_csv() accordingly.
Key Performance Indicators
The initial analysis produced the following results:
KPI	Result
Total deliveries	500
On-time deliveries	235
Delayed deliveries	265
On-time delivery rate	47.00%
Delivery delay rate	53.00%
Average actual delivery time	422.44 minutes
Average delivery cost	₹475.11


Formulas
- On-time delivery rate = (On-time deliveries / Total deliveries) × 100
- Delivery delay rate = (Delayed deliveries / Total deliveries) × 100
- Average delivery time = Total actual delivery minutes / Total deliveries
- Average delivery cost = Total delivery cost / Total deliveries
Initial Exploratory Findings
- The overall delay rate is 53% in this simulated dataset.
- The average delay by traffic category is approximately 25.12 minutes for High traffic, 3.22 minutes for Medium traffic, and -18.52 minutes for Low traffic. Negative delay means delivery was early on average.
- The average delay by weather is approximately 28.59 minutes for Storm, 10.38 minutes for Rain, and -4.49 minutes for Clear conditions.
- Delayed orders have an average distance of 266.26 km, compared with 244.21 km for on-time orders.
- Delayed orders have an average delivery cost of ₹502.64, compared with ₹444.06 for on-time orders.
- The average actual delivery time is 448.53 minutes for delayed orders and 393.02 minutes for on-time orders.
These are descriptive findings, not proof of causation. Results may be influenced by multiple factors, such as distance, traffic, weather, and vehicle allocation. The dataset is simulated, so findings should be validated using real operational data before making business decisions.
Proposed Next Steps
1. Complete and document data cleaning and exploratory data analysis.
2. Investigate relationships among distance, traffic, weather, vehicle type, cost, and delivery delays.
3. If suitable real data becomes available, develop a classification model to predict whether a delivery may be delayed.
4. Evaluate the model with appropriate metrics such as precision, recall, F1-score, and a confusion matrix.
5. Explore route and resource optimization to reduce delays and delivery costs.
6. Summarize recommendations and limitations in the final report.
Project Deliverables
- Exploratory analysis notebook in notebook/
- Dataset in data/
- Strategic planning report in report/
Author
Created as a  learning project on strategic planning and data exploration in logistics.
